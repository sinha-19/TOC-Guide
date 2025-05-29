# 03. Languages and Grammars

---

## What is a Language?

In TOC, a **language** is a set of strings formed from an alphabet (Σ).

- **Alphabet (Σ):** A finite, non-empty set of symbols (e.g., Σ = {0,1})
- **String:** Finite sequence of symbols from Σ (e.g., 0101)
- **Language (L):** Subset of Σ* (all finite strings over Σ)

### Examples

- L = {w | w has an even number of 0s}
- L = {ε, 0, 1, 00, 11, 010, ...}
- L = set of all palindromes over {a, b}

---

## Operations on Languages

- **Union:** L1 ∪ L2
- **Intersection:** L1 ∩ L2
- **Concatenation:** L1L2 = {xy | x ∈ L1, y ∈ L2}
- **Kleene Star:** L* = {w1w2...wn | n ≥ 0, wi ∈ L}
- **Complement:** Σ* - L

---

## What is a Grammar?

A **grammar** G is a formal description of a language.

- **G = (V, Σ, R, S)**
    - V: Non-terminal symbols
    - Σ: Terminal symbols (alphabet)
    - R: Productions (rules)
    - S: Start symbol (S ∈ V)

### Example (CFG for balanced parentheses)

- V = {S}
- Σ = {(, )}
- R: S → SS | (S) | ε

---

## Types of Grammars (Chomsky Hierarchy)

1. **Type 3:** Regular Grammars (finite automata)
2. **Type 2:** Context-Free Grammars (CFGs, PDAs)
3. **Type 1:** Context-Sensitive Grammars (linear bounded automata)
4. **Type 0:** Unrestricted Grammars (Turing machines)

---

## Derivations and Parse Trees

- **Derivation:** Sequence of rule applications to generate a string from S.
- **Parse Tree:** Tree representation of derivation.

---

## Ambiguity

- A grammar is **ambiguous** if some string has more than one leftmost or rightmost derivation (or parse tree).
- Ambiguous grammars are problematic for programming languages.

---

## Language Descriptions

- **Descriptive:** "Set of all strings with at least two 1s"
- **Formal:** L = {w ∈ {0,1}* | w contains at least two 1s}

---

## Applications

- Regular languages: Lexical analysis, pattern matching
- Context-free languages: Programming language syntax
- Context-sensitive: Some natural languages
- Recursively enumerable: General computation

---

## Interview Patterns

- Write a grammar for a given language.
- Identify if a grammar is ambiguous.
- Construct the complement of a given language.
- Express a language using set operations.

---

## Common Pitfalls

- Mixing up terminals and non-terminals.
- Forgetting the base case (ε) in recursive rules.
- Overcomplicating or oversimplifying a grammar.

---

## Exercises

1. Write a grammar for the set of palindromes over {a, b}.
2. Show that the language {anbn | n ≥ 0} is context-free but not regular.
3. Give an example of an ambiguous grammar.
4. For L = {w | w contains equal number of 0s and 1s}, is L regular? Why or why not?
5. Write the regular expression for L = {w | w contains at least one '01'}.

---

## Key Interview Questions

- How do you determine if a language is regular?
- What is the importance of ambiguity in grammars?
- How do operations on languages relate to automata?

---

## Summary

Formal languages and grammars underpin automata, parsing, and programming language theory. Mastery here is essential for advanced TOC topics and interviews.

---
