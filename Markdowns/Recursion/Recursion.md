## Core Recursion Pattern
--------------------------------------------------------------------------------
- Big to small sub problems.
- Ek baar problem solve hone ke baad input variable me ky change aayega.
--------------------------------------------------------------------------------
- Each call does:
  1) Process current state
  2) Reduce problem size
  3) Delegate to smaller subproblem
- Control returns AFTER recursive call completes

Two valid orders:
- Process → Recurse
- Recurse → Process

(Choose based on problem requirement)

---

## Key Invariants (Must Always Hold)
- Each recursive call reduces input size
- Base case is reachable
- No array / string access before base case check
- Stack depth ≤ problem size

---

## Base Case Rules (Non-Negotiable)
- Base case check ALWAYS before:
  - array access
  - recursive call
- Base case must STOP further calls completely

---

## Common Failure Modes (Observed)
- Forgetting base case → infinite recursion
- Base case after array access → runtime error
- No size reduction → stack overflow
- Confusing work per call with number of calls

---

## Time & Space Thinking (Simple Model)
- Time = (work per call) × (number of calls)
- Space = maximum recursion depth (call stack)

If recursion tree branches:
- Count calls using tree, not intuition

---

## Prevention Rules
- Write base case FIRST
- Explicitly state what changes in each call
- Before coding, answer:
  - What decreases?
  - When does it stop?
  - How deep can stack go?

---

## Anchor Problems (Mental References)
- Print numbers (pre/post recursion)
- Factorial
- Fibonacci

