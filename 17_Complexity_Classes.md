# 17. Complexity Classes (P, NP, NP-Complete, NP-Hard)

---

## What is Computational Complexity?

**Computational complexity** studies the resources (time, space) required to solve computational problems. It’s about how hard a problem is, not just whether it’s solvable.

---

## Time Complexity and Space Complexity

- **Time complexity:** Number of steps an algorithm takes as a function of input size n.
- **Space complexity:** Amount of memory used.

---

## Big-O Notation

- Describes asymptotic upper bounds.
- E.g., O(n), O(n²), O(2ⁿ)

---

## Complexity Classes

### 1. P (Polynomial Time)

- Class of decision problems solvable by a deterministic Turing machine in polynomial time (O(nᵏ) for some k).
- “Efficiently solvable” problems.

### 2. NP (Non-deterministic Polynomial Time)

- Problems for which a solution can be **verified** in polynomial time.
- Equivalently, solvable by a non-deterministic TM in polynomial time.

### 3. NP-Complete

- Problems in NP that are as “hard” as any other NP problem.
- If any NP-complete problem can be solved in polynomial time, then **P = NP**.
- To prove a problem is NP-complete:
    1. Show it’s in NP.
    2. Reduce a known NP-complete problem to it in polynomial time.

### 4. NP-Hard

- At least as hard as the hardest problems in NP.
- Not necessarily in NP (can be optimization or undecidable problems).

### 5. co-NP

- The class of problems whose complements are in NP.

---

## P vs NP

- **Open question**: Is P = NP?
- If yes, every efficiently verifiable problem is efficiently solvable.
- Most believe P ≠ NP.

---

## Examples

- **P:** Sorting, shortest path (Dijkstra’s), primality test.
- **NP:** SAT (boolean satisfiability), subset sum, Hamiltonian path.
- **NP-Complete:** SAT, 3SAT, clique, vertex cover, subset sum.
- **NP-Hard:** Halting problem, optimization versions of NP-complete problems.

---

## Reductions in Complexity

- **Polynomial-time reduction:** Used to show NP-completeness.
- If A reduces to B and B is “easy”, then A is “easy”.

---

## Cook-Levin Theorem

- SAT is NP-complete (first NP-complete problem).

---

## Space Complexity Classes

- **PSPACE:** Problems solvable with polynomial space.
- **L:** Logarithmic space.
- **NL:** Non-deterministic logarithmic space.

---

## Hierarchy of Classes

P ⊆ NP ⊆ PSPACE ⊆ EXPTIME

- All inclusions are believed to be proper, but only P ⊆ NP is open.

---

## Interview Patterns

- Classify a problem as P, NP, NP-complete, or NP-hard.
- Show a problem is in NP.
- Prove NP-completeness via reduction.
- Discuss implications of P = NP.

---

## Common Pitfalls

- Confusing “verifiable in poly time” with “solvable in poly time”.
- Assuming all NP problems are hard (some are in P).
- Mixing up NP-complete and NP-hard.

---

## Exercises

1. Prove that the Subset Sum problem is NP-complete.
2. Is the Traveling Salesman Problem (decision version) NP-complete or NP-hard?
3. Show that Vertex Cover is NP-complete.
4. Discuss why the Halting Problem is not in NP.

---

## Key Interview Questions

- What is the difference between P and NP?
- What does it mean for a problem to be NP-complete?
- Explain polynomial-time reduction.
- Why is P vs NP important?

---

## Summary

Understanding complexity classes helps you judge the tractability of problems, design efficient algorithms, and recognize computational limits.

---
