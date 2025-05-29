# 02. Sets, Relations, and Functions

---

## What are Sets?

A **set** is a well-defined collection of distinct objects, considered as an object in its own right. Sets are foundational in mathematics and computer science.

- **Notation:** {a, b, c}, ∅ (empty set)
- **Examples:** Set of all natural numbers, set of states in an automaton

### Basic Operations

- **Union (A ∪ B):** Elements in A or B or both
- **Intersection (A ∩ B):** Elements in both A and B
- **Difference (A - B):** Elements in A but not in B
- **Complement (A̅):** Elements not in A (relative to a universal set)

### Properties

- Commutative: A ∪ B = B ∪ A
- Associative: (A ∪ B) ∪ C = A ∪ (B ∪ C)
- Distributive: A ∩ (B ∪ C) = (A ∩ B) ∪ (A ∩ C)

---

## Cartesian Product

- **A × B = {(a, b) | a ∈ A, b ∈ B}**
- Used to define relations and functions.

---

## What are Relations?

A **relation** R from set A to set B is a subset of A × B.

- **Examples:**
    - Equality relation: R = {(a, a) | a ∈ A}
    - "Divides": R = {(a, b) | a divides b}

### Properties of Relations

- **Reflexive:** (a, a) ∈ R for all a
- **Symmetric:** (a, b) ∈ R ⇒ (b, a) ∈ R
- **Transitive:** (a, b) ∈ R and (b, c) ∈ R ⇒ (a, c) ∈ R
- **Equivalence Relation:** Reflexive, symmetric, transitive

### Equivalence Classes

Partition a set into disjoint subsets where every element is related.

---

## Functions

A **function** f from A to B associates each element of A with exactly one element of B.

- **Notation:** f: A → B, f(a) = b

### Types of Functions

- **Injective (One-to-one):** f(a) = f(b) ⇒ a = b
- **Surjective (Onto):** Every b ∈ B is f(a) for some a ∈ A
- **Bijective:** Both injective and surjective

---

## Functions in TOC

- **Transition functions:** δ in automata (e.g., δ: Q × Σ → Q)
- **Encoding/decoding:** Mapping strings to numbers, etc.

---

## Power Set

- The set of all subsets of a set A, denoted 2^A.
- Important when analyzing the state space of automata (e.g., NFA to DFA conversion).

---

## Applications in Theory of Computation

- States, alphabets, and transitions in automata are all sets.
- Relations define transition functions, language acceptance.
- Functions are used for state transitions, encodings, mappings.

---

## Interview Patterns

- Given a relation, prove or disprove it's an equivalence relation.
- Construct the power set for a given set.
- Use set operations to explain language operations (union, intersection, etc.).

---

## Common Mistakes

- Confusing subset ⊆ and element ∈.
- Not checking all properties for relations.
- Forgetting that functions must map every element of the domain.

---

## Exercises

1. Prove that the "is sibling of" relation is symmetric but not transitive.
2. Find the power set of {a, b, c}.
3. Give an example of a function that is injective but not surjective.
4. For the set of integers ℤ, is the "less than" relation transitive? Reflexive? Symmetric?
5. Express the intersection of two languages as a set operation.

---

## Key Interview Questions

- What is the difference between a relation and a function?
- How do you prove a relation is an equivalence relation?
- Why is the power set important in NFA to DFA conversion?
- How are set operations related to language operations?

---

## Summary

Understanding sets, relations, and functions is fundamental for all topics in TOC, especially automata, grammars, and computability.

---
