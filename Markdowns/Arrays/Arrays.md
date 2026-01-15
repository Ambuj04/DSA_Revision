## Core Patterns
- Sliding Window
- Two Pointers
- Kadane’s Algorithm (Dynamic Window)

---

## Key Invariants (Must Hold)

### Kadane
- At each index, I track the best subarray ending HERE
- If current sum < 0 → discard and restart
- Global max is updated at every step

### Sliding Window
- Window expands and shrinks based on condition
- Left pointer only moves forward
- Window always represents a valid subarray

---

## Edge Cases (Non-Negotiable)
- All elements negative (Kadane must handle)
- Single element array
- Large input size (O(n²) will TLE)
- Integer overflow (sum can exceed int)
- Window boundaries (off-by-one)

---

## Common Failure Modes (Observed)
- Defaulting to brute force without checking constraints
- Forgetting all-negative case in Kadane
- Using `for-each` when index is required
- Assuming segmentation fault is random, not logical

---

## Time & Space Thinking
- Brute force subarray → O(n²)
- Kadane / Sliding window → O(n)
- Space is constant unless extra array used

---

## Prevention Rules
- Always check constraints BEFORE coding
- If problem asks max subarray → think Kadane first
- Never use for-each when index logic matters
- Segmentation fault = loop boundary violation, not mystery

---

## Anchor Problems
- Maximum Subarray (Kadane)
- Fixed-size window problems
- Variable-size window problems
