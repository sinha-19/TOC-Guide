# 06. Regular Expressions and Languages

---

## What is a Regular Expression?

A **regular expression** (regex) is a concise, formal way to describe a set of strings over a given alphabet. Regular expressions correspond exactly to regular languages.

---

## Syntax of Regular Expressions

- **Symbols:** a (matches 'a'), ε (matches empty string), ∅ (matches nothing)
- **Union:** r1 + r2 (matches strings in r1 or r2)
- **Concatenation:** r1 r2 (matches strings from r1 followed by r2)
- **Kleene Star:** r* (zero or more repetitions of r)
- **Parentheses:** (r) groups subexpressions

**Example:** (a+b)*abb matches all strings ending with abb

---

## Building Regular Expressions

- **Base cases:** a, ε, ∅ are regular expressions
- **Recursion:** If r and s are regular expressions, so are r+s, rs, r*

---

## Language of a Regular Expression

- **L(a):** {a}
- **L(ε):** {ε}
- **L(∅):** ∅
- **L(r+s):** L(r) ∪ L(s)
- **L(rs):** L(r) ⋅ L(s) (concatenation)
- **L(r*):** (L(r))*

---

## Examples

- L((a+b)*) = set of all strings over {a, b}
- L(a*b*) = strings of a's followed by b's (e.g., aabbb)
- L((ab)*) = even-length strings with alternating a and b

---

## Equivalence of Regular Expressions and Finite Automata

- For every regular expression, there is an NFA (and thus a DFA) that recognizes the same language.
- For every DFA/NFA, a regular expression can be constructed that describes its language.

---

## Converting Regex to NFA (Thompson’s Construction)

- Each base case and operator has a construction template.
  - **a:** Two states, transition on a
  - **ε:** Two states, ε-transition
  - **Union:** New start/end, ε to each sub-NFA
  - **Concatenation:** Join end of first to start of second
  - **Kleene Star:** New start/end, ε-loops

---

## Converting DFA to Regex (State Elimination Method)

- Remove states one by one, updating transitions with regular expressions, until only start and accept remain.
- Final expression describes the language.

---

## Properties of Regular Languages

- **Closed under:** Union, concatenation, star, intersection, complement, difference, reversal
- **Not closed under:** Some operations (e.g., context-sensitive substitutions)

---

## Applications

- Lexical analyzers, grep, text editors
- Pattern matching in programming languages
- Input validation

---

## Limitations

- Cannot express languages with nested or balanced parentheses (non-regular)
- Cannot count arbitrarily (e.g., L = {a^n b^n | n ≥ 0})

---

## Interview Patterns

- Write a regex for a given language
- Convert regex to NFA or DFA
- Prove a language is not regular (e.g., using the pumping lemma)
- Show two regexes are equivalent

---

## Common Mistakes

- Misinterpreting precedence: * > concatenation > +
- Forgetting ε in cases like (a+b)*
- Overusing regex for non-regular problems

---

## Exercises

1. Write a regex for strings over {0,1} where every 0 is immediately followed by a 1.
2. Convert the regex (ab)* + b* to an NFA.
3. Show that L = {w | w contains an even number of a's} is regular and give a regex.
4. Find a regex for all binary strings that do not contain '11'.
5. Prove that palindromes are not regular.

---

## Key Interview Questions

- How do you convert a regex to an NFA?
- Can regular expressions describe all languages? Why/why not?
- What are the closure properties of regular languages?
- Give an example of a language that can be described by regex but not by a context-free grammar (trick: all regexes are also CFGs, but not vice versa).

---

## Summary

Regular expressions are a powerful tool for describing regular languages. Understanding their construction, conversion, and limitations is essential for both interviews and real-world application.

---
