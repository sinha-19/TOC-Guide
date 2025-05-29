# 19. Interview Patterns, Proofs, and Q&A

---

## 1. Automata Construction

- **Pattern:** Given a language, construct a DFA/NFA or regex.
  - “Design a DFA for all strings ending with 01 over {0,1}.”
  - “Convert the regex (ab)* to a DFA.”

**Tips:**
  - Draw the state diagram.
  - Justify transitions and accept states.

---

## 2. Proving Non-Regularity

- **Pattern:** Use the pumping lemma.
  - “Prove {a^n b^n | n ≥ 0} is not regular.”

**Tips:**
  - State the lemma.
  - Choose s = a^p b^p.
  - Show contradiction by pumping y.

---

## 3. CFG and PDA Construction

- “Write a CFG for palindromes.”
- “Design a PDA for {a^n b^n | n ≥ 0}.”

**Tips:**
  - Identify recursive patterns.
  - Use stack for counting/matching.

---

## 4. Proving Non-Context-Freeness

- “Show L = {a^n b^n c^n | n ≥ 0} is not context-free.”
- Use the CFL pumping lemma.

---

## 5. Closure Properties

- “Are regular languages closed under intersection?”
- “Give an example where CFLs are not closed under intersection.”

**Tips:** Provide a counterexample if not closed.

---

## 6. Decidability & Undecidability

- “Is the halting problem decidable?”
- “Use reduction to show problem X is undecidable.”

**Tips:**
  - Reference the Halting Problem.
  - Describe the reduction.

---

## 7. Complexity Classification

- “Is Subset Sum in NP?”
- “Show SAT is NP-complete.”

**Tips:**
  - Show membership in NP.
  - Reduce from a known NP-complete problem.

---

## 8. Problem Identification

- “Given a language, is it regular, context-free, or neither?”
- “Is this problem in P, NP, or NP-complete?”

---

## 9. Proofs and Constructions

- Always define your terms and models.
- State assumptions and known results.
- Use clear, step-by-step logic.

---

## 10. Explaining Theorems

- “What is Rice’s Theorem?”
- “Explain the Church–Turing Thesis.”

---

## 11. Q&A Quick Reference

- **How to prove non-regularity?** Use pumping lemma.
- **How to show a language is regular/context-free?** Construct DFA/NFA/CFG.
- **How to prove undecidability?** Reduce from a known undecidable problem.
- **What is NP-completeness?** In NP, as hard as any NP problem.
- **How to classify a language/problem?** Map to known classes.

---

## 12. Behavioral Patterns

- Clarify requirements.
- Communicate your thought process.
- Draw diagrams and explain logic.
- Justify each step and choice.
- Be ready to handle follow-up and edge cases.

---

## 13. Practice Problems

1. Design a DFA for binary strings divisible by 3.
2. Use the pumping lemma to show L = {ww | w ∈ {0,1}*} is not regular.
3. Write a CFG for all palindromes over {a, b}.
4. Prove the Halting Problem is undecidable.
5. Show 3SAT is NP-complete.

---

## 14. Resources

- **Books:** Sipser, Hopcroft & Ullman, Papadimitriou
- **Online:** GeeksforGeeks, Brilliant.org, MIT OCW
- **Practice:** LeetCode, Codeforces (for algorithmic thinking)

---

## 15. Tips for Success

- Practice constructions and proofs on paper.
- Memorize key theorems and their applications.
- Explain your reasoning clearly and confidently.
- Review common closure properties and proof templates.
- Don’t be afraid to ask clarifying questions in interviews.

---

## Summary

TOC interviews are about construction, proof, and clear communication. With practice and a systematized approach, you can master them and demonstrate deep understanding.

---
