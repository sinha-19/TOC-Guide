# 16. Reducibility and Recursively Enumerable Languages

---

## What is Reducibility?

**Reducibility** is a fundamental concept in computability theory. It’s a way of relating the difficulty of decision problems by showing how one can be transformed into another.

---

## Types of Reducibility

### 1. Mapping Reducibility (Many-One, ≤ₘ)

- Language A is **mapping reducible** to language B (A ≤ₘ B) if there is a computable function f such that for all x:  
  x ∈ A ⇔ f(x) ∈ B
- If B is decidable and A ≤ₘ B, then A is decidable.

### 2. Turing Reducibility

- A is **Turing reducible** to B if a decider for B (an oracle) can be used to decide A.

---

## Why Reducibility Matters

- It lets us prove undecidability: reduce a known undecidable problem to a new one.
- It helps create a hierarchy of problems.
- Central for NP-completeness and complexity theory.

---

## Recursively Enumerable (RE) Languages

- A language L is **recursively enumerable (RE)** if there exists a Turing machine that will accept every string in L (but may not halt for strings not in L).
- All decidable (recursive) languages are RE, but not all RE languages are decidable.

---

## Properties of RE Languages

- **Closed under:** Union, intersection, concatenation, Kleene star.
- **Not closed under:** Complement.
- If L is RE, its complement may not be RE.

---

## Examples

- The set of Turing machines that halt on input w is RE (but not decidable).
- The halting problem’s complement is not RE.

---

## Post Correspondence Problem (PCP)

- A classic undecidable problem.
- Given two lists of strings, is there a sequence of indices such that the concatenated strings match?
- PCP is RE (solutions can be checked by enumeration), but undecidable.

---

## Reductions in Action

- To prove a new problem is undecidable, reduce from a known undecidable one (e.g., Halting Problem, PCP).

---

## Rice’s Theorem (Revisited)

- Any nontrivial property of RE languages (properties that are true for some but not all RE languages) is undecidable.

---

## Applications

- Proving language properties are undecidable.
- Establishing equivalence and hardness in complexity theory.

---

## Interview Patterns

- Show a language is RE but not recursive.
- Prove undecidability by mapping reduction.
- Explain why the complement of an RE language may not be RE.

---

## Common Pitfalls

- Confusing RE with recursive languages.
- Not constructing the computable function in mapping reducibility.
- Not checking closure properties.

---

## Exercises

1. Show that the Halting Problem is RE but not recursive.
2. Explain why the complement of the Halting Problem is not RE.
3. Use mapping reduction to prove PCP is undecidable.
4. Give an example of a language that is not RE.

---

## Key Interview Questions

- What is a recursively enumerable language?
- What is mapping reducibility? Why is it important?
- What is Rice’s Theorem?

---

## Summary

Reducibility and recursively enumerable languages are central to understanding the boundaries of computability and the relationships between decision problems.

---
