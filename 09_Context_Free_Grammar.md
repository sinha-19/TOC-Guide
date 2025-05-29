# 09. Context-Free Grammars (CFGs)

---

## What is a Context-Free Grammar?

A **context-free grammar** (CFG) is a formal grammar that generates context-free languages (CFLs). CFGs are widely used in programming languages and compilers.

---

## Components of a CFG

A CFG is a 4-tuple (V, Σ, R, S):
- V: Finite set of non-terminals (variables)
- Σ: Finite set of terminals (alphabet)
- R: Set of production rules (A → α, where A ∈ V, α ∈ (V ∪ Σ)*)
- S: Start symbol (S ∈ V)

---

## How CFGs Work

- Start from S.
- Apply production rules to derive strings of terminals.
- All strings derived form the language L(G).

---

## Example CFG: Balanced Parentheses

- S → SS | (S) | ε

---

## Parse Trees and Derivations

- **Parse Tree:** Shows application of rules, root is S, leaves are terminals or ε.
- **Leftmost/Rightmost Derivation:** Always expand the leftmost/rightmost non-terminal first.

---

## Ambiguity

- A grammar is **ambiguous** if a string has multiple parse trees (or leftmost/rightmost derivations).
- Ambiguity is problematic for parsing programming languages.

---

## Chomsky Normal Form (CNF)

- All rules are A → BC or A → a.
- Any CFG can be converted to CNF.
- Useful for algorithms (e.g., CYK parsing).

---

## Regular Languages are Context-Free

- All regular languages can be described by a CFG (but not vice versa).

---

## Applications

- Programming language syntax
- Simple expression evaluation
- Natural language processing

---

## Limitations

- Cannot describe all languages (e.g., {a^n b^n c^n | n ≥ 0} is not CFL)
- Ambiguous grammars may not be avoidable for some languages

---

## Pushdown Automata (PDA)

- Equivalent in power to CFGs.
- Uses a stack to store information.

---

## Closure Properties

- CFLs are closed under union, concatenation, star.
- Not closed under intersection or complement.

---

## Interview Patterns

- Write a CFG for a given language (e.g., palindromes, balanced brackets).
- Show a language is not context-free (pumping lemma for CFLs).
- Convert a CFG to CNF.
- Identify if a CFG is ambiguous.

---

## Common Pitfalls

- Confusing terminals with non-terminals.
- Forgetting ε-productions (for empty strings).
- Not minimizing or simplifying rules.

---

## Exercises

1. Write a CFG for L = {a^n b^n | n ≥ 0}.
2. Show that L = {ww | w ∈ {a, b}*} is not context-free.
3. Convert S → aSb | SS | ε to CNF.
4. Give an example of an inherently ambiguous language.
5. Write a CFG for arithmetic expressions with + and *.

---

## Key Interview Questions

- What is a context-free grammar? Give an example.
- How do you prove a language is not context-free?
- What is Chomsky Normal Form and why is it useful?

---

## Summary

Context-free grammars describe a vast class of languages, including most programming language syntax. They are a key tool for both theory and practice.

---
