# 13. Turing Machines (TM)

---

## What is a Turing Machine?

A **Turing Machine** is a mathematical model of computation with an infinite tape and a read/write head. It is the most powerful simple model, capable of simulating any algorithm.

---

## Components of a Turing Machine

A TM is a 7-tuple (Q, Σ, Γ, δ, q0, q_accept, q_reject):

- Q: Finite set of states
- Σ: Input alphabet (does not include the blank symbol)
- Γ: Tape alphabet (includes Σ and blank symbol ␣)
- δ: Transition function (Q × Γ → Q × Γ × {L, R})
- q0: Start state
- q_accept: Accept state
- q_reject: Reject state (q_accept ≠ q_reject)

---

## How a TM Works

- The tape is infinite in both directions, filled with blanks.
- The head reads a symbol, writes a new symbol, moves left or right, and transitions to a new state.
- Accept/reject by entering q_accept or q_reject.

---

## Types of Turing Machines

- **Deterministic TM (DTM):** δ is a function.
- **Non-deterministic TM (NTM):** δ gives a set of possible moves; equivalent in power to DTM.

---

## Turing-Recognizable (Recursively Enumerable) Languages

- Set of languages that some TM accepts (possibly non-terminating on some inputs).

---

## Turing-Decidable (Recursive) Languages

- Set of languages for which some TM always halts (accepts or rejects).

---

## Church–Turing Thesis

- Every effectively computable (algorithmic) function can be computed by a TM.

---

## Universal Turing Machine

- A TM that can simulate any other TM (basis for programmable computers).

---

## Variants of Turing Machines

- **Multi-tape TM:** Multiple tapes/heads; more efficient but not more powerful.
- **Non-deterministic TM:** Equivalent in power to DTM.
- **TM with infinite alphabet:** Still equivalent in power.

---

## TM vs. Other Models

- More powerful than PDAs and FAs.
- Can recognize languages not recognized by any PDA or FA.

---

## Applications

- Models for computation and algorithms.
- Basis for decidability and complexity theory.

---

## Interview Patterns

- Design a TM for a simple language (e.g., L = {ww | w ∈ {0,1}*}).
- Prove a language is Turing-recognizable but not decidable.
- Discuss the halting problem.

---

## Common Pitfalls

- Confusing Turing-recognizable and Turing-decidable.
- Assuming non-determinism increases power for TMs (it does not).
- Forgetting that TMs can run forever.

---

## Exercises

1. Design a TM for L = {a^n b^n c^n | n ≥ 0}.
2. Explain the difference between a TM and a PDA.
3. Prove that the halting problem is undecidable.
4. Describe how a universal TM works.

---

## Key Interview Questions

- What is a Turing machine?
- What languages can a TM recognize?
- What is the significance of the Church–Turing Thesis?
- What is the halting problem?

---

## Summary

Turing Machines define the boundaries of computability and underpin all modern computation theory. Understanding TMs is essential for advanced CS interviews.

---
