# 08. Pumping Lemma for Regular Languages

---

## What is the Pumping Lemma?

The **pumping lemma** is a proof technique used to show that a language is **not** regular. It states that for any regular language, long enough strings can be "pumped" (a section repeated any number of times) and still belong to the language.

---

## Formal Statement

For every regular language L, there exists an integer p (pumping length) such that for every string s ∈ L with |s| ≥ p:

- There exist strings x, y, z such that:
  1. s = xyz
  2. |y| > 0
  3. |xy| ≤ p
  4. For all i ≥ 0, the string xy^i z ∈ L

---

## How to Use the Pumping Lemma

1. **Assume L is regular.** (For contradiction)
2. **Let p be the pumping length.**
3. **Choose a string s ∈ L with |s| ≥ p.**
4. **Consider all possible ways to split s = xyz** (with |y| > 0, |xy| ≤ p).
5. **Show that for some i (often 0 or 2), xy^i z ∉ L.**
6. **Contradiction ⇒ L is not regular.**

---

## Example: L = {a^n b^n | n ≥ 0}

Assume L is regular with pumping length p.

- Choose s = a^p b^p ∈ L.
- For any split s = xyz, with |xy| ≤ p, y consists only of a's.
- Let y = a^k, k > 0.
- Pump y: xy^2z = a^{p+k} b^p (more a's than b's) ∉ L.
- Contradiction ⇒ L is not regular.

---

## Common Patterns

- Use s with repeated structure (e.g., a^p b^p).
- y falls within a "homogeneous" section (e.g., all a's).
- Pumping y (repeat or remove) destroys the required pattern.

---

## What the Pumping Lemma Does NOT Do

- It **cannot** be used to prove a language **is** regular (only to prove non-regularity).
- Failing to find a contradiction does not prove regularity.

---

## Tips for Effective Use

- Choose the hardest possible string s (often length exactly p).
- Consider all possible splits, not just one.
- Try i = 0 (remove y) and i = 2 (repeat y).

---

## Common Mistakes

- Only considering one split of s.
- Not justifying that y ≠ ε and |xy| ≤ p.
- Using the pumping lemma to prove regularity.

---

## Advanced: Pumping Lemma Variants

- Some non-regular languages can "pass" the pumping lemma for some p (but fail for all sufficiently large p).
- There are stronger theorems (e.g., Ogden's Lemma) for more complex languages.

---

## Exercises

1. Use the pumping lemma to show L = {w ∈ {0,1}* | w is a palindrome} is not regular.
2. Prove L = {a^i b^j | i ≠ j} is not regular.
3. Show that L = {w | number of a's = number of b's} over {a, b} is not regular.
4. Why can't you use the pumping lemma to prove regularity?
5. For L = {a^p | p is a prime number}, show non-regularity.

---

## Key Interview Questions

- State the pumping lemma for regular languages.
- How do you use the pumping lemma to prove a language is not regular?
- What are the limitations of the pumping lemma?

---

## Summary

The pumping lemma is a vital tool for disproving regularity. Mastering its use is key for theoretical proofs and technical interviews.

---
