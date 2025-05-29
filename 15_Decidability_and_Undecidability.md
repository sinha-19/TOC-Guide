# 15. Decidability and Undecidability

---

## What is Decidability?

A problem (language) is **decidable** if there exists a Turing machine that always halts and correctly decides membership for any input string (accepts or rejects).

- **Decidable language:** Also called recursive language.

---

## What is Undecidability?

A problem is **undecidable** if no such Turing machine exists (i.e., some inputs cause the machine to run forever).

- **Recursively enumerable (RE):** Recognized (but not necessarily decided) by a TM; TM may loop forever for some inputs.
- **Co-RE:** Complements of RE languages.

---

## Examples of Decidable Problems

- Membership for regular languages (DFA/NFA)
- Membership for CFLs (CFGs, via CYK parsing)
- Emptiness, finiteness for DFA
- Equivalence of regular languages

---

## Examples of Undecidable Problems

- **Halting Problem:** "Given a TM M and input w, does M halt on w?"
- **TM Accepts Empty String:** Does M accept ε?
- **Post Correspondence Problem**

---

## Halting Problem

- **Formally:** L = {⟨M, w⟩ | TM M halts on input w}
- Proven undecidable by reduction (diagonalization).

---

## Reductions

- To show a problem is undecidable, reduce from a known undecidable problem (e.g., Halting Problem).
- **Mapping reduction:** If A ≤_m B and A is undecidable, then B is undecidable.

---

## Rice's Theorem

- All nontrivial semantic properties of Turing-recognizable languages are undecidable.
- "Nontrivial": Some TMs have the property, some do not.

---

## Recognizability

- **Turing-recognizable (RE):** There exists a TM that accepts all strings in L (may loop forever otherwise).
- **Turing-decidable (Recursive):** The TM halts on all inputs.

---

## Semi-Decidable Problems

- Problems where "yes" answers are recognizable, "no" answers may loop forever.

---

## Decidability Table

| Problem                          | Decidable? | Recognizable? |
|-----------------------------------|------------|---------------|
| DFA emptiness                    | Yes        | Yes           |
| CFG membership                   | Yes        | Yes           |
| TM halting on input              | No         | Yes           |
| TM equivalence                   | No         | No            |

---

## Applications

- Proving limits of computation.
- Understanding what compilers and analyzers can detect.

---

## Interview Patterns

- Prove undecidability using reduction from the Halting Problem.
- Classify problems as decidable, RE, co-RE, or neither.
- Explain Rice's theorem and apply it.

---

## Common Pitfalls

- Believing all problems are decidable.
- Not using reduction correctly.
- Assuming that recognizability implies decidability.

---

## Exercises

1. Prove that the language L = {⟨M⟩ | M halts on input 0} is undecidable.
2. Use Rice's Theorem to show "TM M accepts all inputs" is undecidable.
3. Distinguish between decidable, RE, and co-RE languages.
4. Show that the Post Correspondence Problem is undecidable.

---

## Key Interview Questions

- What is the halting problem? Why is it undecidable?
- How do you prove a problem is undecidable?
- What is Rice’s Theorem?
- What is the difference between decidability and recognizability?

---

## Summary

Decidability defines the limits of algorithmic computation. Recognizing undecidable problems prevents wasted effort and clarifies what software can and cannot do.

---
