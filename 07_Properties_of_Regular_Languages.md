# 07. Properties of Regular Languages

---

## What is a Regular Language?

A **regular language** is any language that can be recognized by a finite automaton (DFA or NFA), or equivalently, described by a regular expression.

---

## Closure Properties

Regular languages are closed under the following operations:

- **Union:** If L1, L2 are regular, so is L1 ∪ L2.
- **Concatenation:** L1 ⋅ L2 is regular.
- **Kleene Star:** L* is regular.
- **Intersection:** L1 ∩ L2 is regular.
- **Complement:** Σ* - L is regular.
- **Difference:** L1 - L2 is regular.
- **Reversal:** {w^R | w ∈ L} is regular.
- **Homomorphism:** Applying a symbol mapping preserves regularity.
- **Inverse Homomorphism:** Preimage under mapping is regular.

---

## Proof Techniques

### Using Automata

- Construct DFA/NFA for each operation.
- **Union/Intersection:** Product automaton (cross product of states).
- **Complement:** Swap accept/reject states in DFA.

### Using Regular Expressions

- Show regex construction for operations.

---

## Non-Regular Languages

- Not all languages are regular! Examples:
  - L = {a^n b^n | n ≥ 0}
  - L = set of palindromes over {a, b}
  - L = {ww | w ∈ {0,1}*}

---

## Pumping Lemma for Regular Languages

A critical tool to prove that a language is **not** regular.

- For every regular language L, there exists a constant p (pumping length) such that:
    - Any string s ∈ L with |s| ≥ p can be divided into s = xyz, satisfying:
        1. |y| > 0
        2. |xy| ≤ p
        3. For all i ≥ 0, xy^i z ∈ L

---

## Deciding Regularity

- If you can construct a DFA/NFA/regex, the language is regular.
- If not, use the pumping lemma to prove non-regularity.

---

## Minimization

- Every regular language has a unique minimal DFA (up to isomorphism).
- Useful for optimization and equivalence testing.

---

## Myhill–Nerode Theorem

- A language is regular iff it has a finite number of equivalence classes (distinguishable strings).
- Used to prove non-regularity and minimize DFAs.

---

## Decision Algorithms

- Emptiness: Is L = ∅?
- Finiteness: Is L finite?
- Membership: Is w ∈ L?
- Equivalence: Do two DFAs accept the same language?

All are decidable for regular languages.

---

## Applications

- Lexical analyzers in compilers
- Protocol and pattern validation
- Text search and replacement

---

## Interview Patterns

- Prove/disprove closure under an operation.
- Use the pumping lemma to show non-regularity.
- Minimize a DFA; check language equivalence.
- Decide membership using a DFA.

---

## Common Pitfalls

- Misapplying the pumping lemma—must work for all splittings.
- Assuming closure under non-regular operations (e.g., intersection with context-free).
- Forgetting the minimal DFA is unique only up to renaming.

---

## Exercises

1. Show that the set of palindromes over {a, b} is not regular.
2. Prove or disprove: The union of two non-regular languages can be regular.
3. Construct a DFA for the intersection of L1 = strings with even a's and L2 = strings with even b's.
4. Use the pumping lemma to show L = {a^n b^n | n ≥ 0} is not regular.
5. Apply Myhill–Nerode to show a language is not regular.

---

## Key Interview Questions

- What is the pumping lemma and how is it used?
- Are regular languages closed under complement? Why?
- How do you minimize a DFA?
- What is the Myhill–Nerode theorem and its significance?

---

## Summary

Regular languages possess strong closure, decision, and minimization properties. Mastering these is vital for both theoretical understanding and practical software engineering.

---
