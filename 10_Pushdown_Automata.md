# 10. Pushdown Automata (PDA)

---

## What is a Pushdown Automaton?

A **pushdown automaton** (PDA) is a computational model like a finite automaton but with a stack. It recognizes context-free languages (CFLs).

---

## Components of a PDA

A PDA is a 7-tuple (Q, Σ, Γ, δ, q0, Z0, F):

- Q: Set of states
- Σ: Input alphabet
- Γ: Stack alphabet
- δ: Transition function (Q × (Σ ∪ {ε}) × Γ → P(Q × Γ*))
- q0: Start state
- Z0: Start stack symbol
- F: Set of accept states

---

## How PDAs Work

- Input is read symbol by symbol.
- At each step, PDA can:
  - Read an input symbol (or ε)
  - Pop a symbol from the stack
  - Push zero or more symbols onto the stack
  - Move to a new state
- Accepts input if it finishes in an accept state (or with empty stack, depending on definition).

---

## Example: PDA for L = {a^n b^n | n ≥ 0}

- Push a symbol for each a.
- For each b, pop a symbol.
- Accept if stack is empty at the end.

---

## Deterministic vs. Non-Deterministic PDA

- Non-deterministic PDAs are more powerful (can accept all CFLs).
- Deterministic PDAs (DPDAs) accept a proper subset of CFLs.

---

## PDAs and CFGs

- For every CFG, there is a PDA that recognizes the same language (and vice versa).

---

## Acceptance by Final State vs. Empty Stack

- Two equivalent ways to define acceptance:
  - By reaching an accept state after consuming all input.
  - By emptying the stack after consuming all input.

---

## Design Techniques

- Use stack to count, match, or remember symbols.
- Non-determinism often needed for palindromes, ww^R, etc.

---

## Limitations

- PDAs cannot recognize all languages (e.g., {a^n b^n c^n | n ≥ 0})
- Stack is LIFO; cannot "remember" arbitrary counts simultaneously.

---

## Applications

- Parsing arithmetic expressions (matching parentheses)
- Syntax analyzers in compilers

---

## Interview Patterns

- Design a PDA for a given language (e.g., palindromes, a^n b^n).
- Convert a CFG to an equivalent PDA.
- Explain why a language cannot be recognized by a PDA.

---

## Common Pitfalls

- Forgetting to define stack operations.
- Using deterministic PDA for inherently ambiguous languages.
- Not handling ε-transitions or empty stack correctly.

---

## Exercises

1. Design a PDA for L = {a^n b^m c^m d^n | n, m ≥ 0}.
2. Convert a CFG for palindromes to a PDA.
3. Explain why {a^n b^n c^n | n ≥ 0} cannot be recognized by a PDA.
4. Show that the set of all strings with equal numbers of a’s and b’s is not context-free.

---

## Key Interview Questions

- What is the power of a PDA compared to a DFA?
- How does a PDA use its stack to recognize context-free languages?
- Can all context-free languages be recognized by a deterministic PDA?

---

## Summary

Pushdown automata extend finite automata with stack memory, enabling recognition of context-free languages. They are the backbone of syntax parsing and language design.

---
