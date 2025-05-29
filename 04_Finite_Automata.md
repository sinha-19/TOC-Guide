# 04. Finite Automata (FA)

---

## What is a Finite Automaton?

A **finite automaton** is a mathematical model of computation with a finite number of states. It reads an input string symbol by symbol and changes state based on a transition function.

---

## Types of Finite Automata

- **Deterministic Finite Automaton (DFA):** For each state and input symbol, exactly one transition.
- **Nondeterministic Finite Automaton (NFA):** For some state and input symbol, multiple transitions or ε (epsilon) transitions are possible.

---

## Formal Definition of DFA

A DFA is a 5-tuple (Q, Σ, δ, q0, F):
- Q: Finite set of states
- Σ: Input alphabet
- δ: Transition function (Q × Σ → Q)
- q0: Start state (q0 ∈ Q)
- F: Set of accept states (F ⊆ Q)

---

## How DFA Works

- Starts at q0.
- For each input symbol, applies δ to move to the next state.
- If after reading all input, the automaton is in a state from F, it accepts; otherwise, it rejects.

---

## Transition Table and Diagram

- **Table:** Rows for states, columns for input symbols, entries for next state.
- **Diagram:** Nodes for states, arrows for transitions, double circle for accept states.

---

## Example: DFA for Even Number of 0’s

States: {q0, q1}
- Start at q0 (even 0's)
- q0 →0→ q1, q1 →0→ q0
- q0 →1→ q0, q1 →1→ q1
- Accept state: q0

---

## NFA Overview

- Like DFA, but:
    - Can have multiple transitions for the same input.
    - Can have ε-transitions (move without consuming input).
- Formally: (Q, Σ, δ, q0, F), but δ: Q × (Σ ∪ {ε}) → P(Q)

---

## DFA vs NFA

- Every NFA can be converted to an equivalent DFA (subset construction).
- NFAs can be simpler to design, but DFAs are easier to implement.

---

## Regular Languages

- A language is **regular** if some DFA (or NFA) recognizes it.
- Regular languages are closed under union, intersection, complement, concatenation, and Kleene star.

---

## Applications

- Lexical analysis in compilers
- Pattern matching (e.g., grep)
- Network protocol parsing

---

## Interview Patterns

- Given a language, design a DFA/NFA.
- Convert an NFA to an equivalent DFA.
- Minimize a DFA.
- Prove a language is not regular using the pumping lemma.

---

## DFA Minimization

- Remove unreachable states.
- Merge equivalent states (partitioning algorithm).

---

## Common Pitfalls

- Forgetting to specify all transitions in a DFA.
- Assuming NFAs are strictly more powerful than DFAs (they are equivalent in power).
- Confusing ε-transitions with actual input symbols.

---

## Exercises

1. Design a DFA that accepts strings over {0,1} ending with '01'.
2. Convert the NFA for (a|b)*ab to a DFA.
3. Minimize the DFA for L = strings over {0,1} with an even number of 1’s.
4. Draw the transition diagram for a DFA recognizing multiples of 3 in binary.

---

## Key Interview Questions

- What is the difference between DFA and NFA?
- Can every NFA be converted to a DFA?
- How do you minimize a DFA?

---

## Summary

Finite automata are foundational for understanding regular languages, lexical analysis, and basic computational models.

---
