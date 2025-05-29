# 12. Pumping Lemma for Context-Free Languages

---

## What is the CFL Pumping Lemma?

The **pumping lemma for context-free languages** is a property that all CFLs satisfy. It's mainly used to show a language is **not** context-free.

---

## Statement of the Pumping Lemma for CFLs

For every context-free language L, there exists a constant p such that every string s ∈ L with |s| ≥ p can be written as s = uvwxy, such that:

1. |vwx| ≤ p
2. vx ≠ ε (at least one of v or x is non-empty)
3. For all i ≥ 0, u(v^i)w(x^i)y ∈ L

---

## How to Use the Pumping Lemma for CFLs

1. **Assume L is context-free.**
2. Let p be the pumping length.
3. Choose s ∈ L, |s| ≥ p.
4. For every way to split s = uvwxy with |vwx| ≤ p and vx ≠ ε,
5. Show that for some i (often i = 0 or 2), u(v^i)w(x^i)y ∉ L.
6. Contradiction ⇒ L is not context-free.

---

## Example: L = {a^n b^n c^n | n ≥ 0}

Assume L is context-free with pumping length p.
- Choose s = a^p b^p c^p.
- For all possible splits uvwxy with |vwx| ≤ p, v and x must be within the same block or span at most two blocks.
- Show that pumping v and x unbalances the counts of a, b, c.
- Thus, for some i, u(v^i)w(x^i)y ∉ L.

---

## Tips for Using the Lemma

- Choose s so that "pumping" will disturb the necessary property (like equal numbers of symbols).
- Consider all possible splits.
- Pump i = 0 (delete v and x) or i = 2 (repeat v and x).

---

## Limitations

- Cannot be used to prove a language **is** context-free (only to show it is not).
- Not all non-context-free languages can be disproved with the regular pumping lemma; the CFL version is more powerful.

---

## Ogden's Lemma

- A generalization where you can "mark" positions in s, making it easier to show non-context-freeness.

---

## Common Pitfalls

- Only considering a single split.
- Not justifying that |vwx| ≤ p and vx ≠ ε.
- Trying to use the lemma to prove context-freeness.

---

## Exercises

1. Use the pumping lemma to show L = {a^n b^n c^n | n ≥ 0} is not context-free.
2. Prove that L = {a^i b^j c^k | i = j or j = k} is not context-free.
3. Use Ogden's lemma for a language where the standard pumping lemma fails.
4. Explain the difference between the regular and CFL pumping lemmas.

---

## Key Interview Questions

- State the pumping lemma for CFLs.
- How do you use the lemma to show a language is not context-free?
- What is Ogden’s lemma and when is it used?

---

## Summary

The pumping lemma for CFLs is a key tool for proving non-context-freeness, essential for both theoretical understanding and interviews.

---
