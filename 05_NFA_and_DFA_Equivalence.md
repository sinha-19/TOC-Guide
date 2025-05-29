# 05. Non-deterministic Finite Automata (NFA) and Equivalence with DFA

---

## What is an NFA?

A **Non-deterministic Finite Automaton (NFA)** is similar to a DFA but allows:
- Multiple possible next states for a given input.
- Transitions without consuming input (ε-transitions).

### Formal Definition

- NFA: (Q, Σ, δ, q0, F)
    - Q: Set of states
    - Σ: Input alphabet
    - δ: Q × (Σ ∪ {ε}) → P(Q) (set of possible states)
    - q0: Start state
    - F: Accept states

---

## How NFAs Work

- At each step, the automaton may choose any valid transition (including ε).
- Accepts if any sequence of choices leads to an accepting state after consuming all input.

---

## ε-Transitions

- Allow state changes without consuming input.
- Useful for simplifying automata constructions.

---

## DFA vs NFA: Equivalence

- **Every NFA has an equivalent DFA.**
- Both recognize exactly the regular languages.

---

## NFA to DFA Conversion (Subset Construction)

1. **States of DFA:** All subsets of NFA states (power set).
2. **Start State:** ε-closure of NFA start state.
3. **Transitions:** For every subset and input, union of reachable states via input (and ε).
4. **Accept States:** Any subset containing an NFA accept state.

---

## Example

**NFA for (a|b)*ab:**
- States: q0 (start), q1, q2 (accept)
- Transitions:
    - q0 --a--> q0, q0 --b--> q0
    - q0 --a--> q1
    - q1 --b--> q2

*Convert to DFA by subset construction.*

---

## Why Use NFAs?

- Easier to construct for many patterns (e.g., regular expressions).
- Simpler for union, concatenation, and star construction.

---

## DFA Minimization After NFA to DFA

- Resulting DFA may have many states.
- Use minimization to reduce state count.

---

## Applications

- Regex engines often use NFAs for initial construction, then convert to DFA for fast matching.
- Protocol design and network filtering.

---

## Common Pitfalls

- Forgetting to include all possible transitions (especially ε-closures).
- Assuming NFA is more powerful than DFA (they are equivalent in expressive power).

---

## Exercises

1. Convert the NFA for L = strings over {0,1} where the third symbol from the end is '1' to a DFA.
2. Draw all possible computation paths for the NFA recognizing (ab|ba)*.
3. Use subset construction to convert a given NFA to a DFA.

---

## Key Interview Questions

- Why are NFAs easier to construct than DFAs?
- How do you convert an NFA with ε-transitions to a DFA?
- Are there languages recognizable by NFA but not DFA?

---

## Summary

NFAs and DFAs are equivalent in recognizing regular languages, but NFAs offer a more flexible and often simpler method for constructing automata.

---
