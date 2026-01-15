## Core Pattern
- Two Pointers:
  - Read pointer scans the string
  - Write pointer builds compressed output in-place
- Processing is done **group by group**, not character by character

---

## Key Invariants (Must Hold)
- Read pointer always points to start of a group
- Write pointer always points to next free position
- Each group is written exactly once
- Count is written only if > 1

---

## Group Processing Logic
For each group of identical characters:
1) Identify group start
2) Count group length
3) Write character
4) Write count digits (if count > 1)

---

## Edge Cases (Must Check)
- Single character string
- All characters unique
- All characters same
- Count ≥ 10 (multi-digit count)
- Last group handling (most common bug)

---

## My High-Risk Mistake (Observed)
- Treated problem as character-by-character instead of group-by-group
- Mixed read and write responsibilities

---

## Prevention Rule
- Read pointer moves only to detect group boundary
- Write pointer moves only after writing group output
- If thinking in characters → stop and reframe as groups

---

## Anchor Problems (Pattern Family)
- LC 443 — String Compression
- Run-Length Encoding
- Remove Consecutive Characters
- Remove Duplicates from Sorted String
- Compress String (GFG / Coding Ninjas)
