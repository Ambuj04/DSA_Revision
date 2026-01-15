## Core Patterns
- **Binary String Generation**
  - Index-based recursion: one recursive call handles exactly one character
  - Branch only when encountering `'?'` → two recursive paths
  - Base case at `index == length`
- **Merge Sort**
  - Divide & Conquer: split array into `[l..mid]` and `[mid+1..r]`
  - Recursion guarantees each half is sorted
  - Merge step combines two sorted halves back into the original array range
- **Quick Sort**
  - Divide & Conquer with pivot selection
  - Partition array around pivot
  - Recursively sort left and right partitions

## Edge Cases
- **Binary String**
  - No `'?'` in string
  - All characters are `'?'`
  - Single-character and empty string
  - Large string → deep recursion (stack overflow risk)
- **Merge Sort**
  - Already sorted array
  - Reverse sorted array
  - Array with duplicate values
  - Single-element or empty range
- **Quick Sort**
  - Already sorted array (worst case for bad pivot choice)
  - All elements equal
  - Very small subarrays (`l >= r`)
  - Pivot at extreme positions

## My Common Mistakes
- **Binary String**
  - Using `==` instead of `=` while assigning `'0'`
  - Mixing loop-based control with index-based recursion
  - Difficulty dry-running due to unclear ownership of `index`
- **Merge Sort**
  - Wrong pointer initialization (`i`, `j` not aligned to subarray ranges)
  - Comparing indices instead of values
  - Inserting multiple elements for one comparison
  - Forgetting to copy remaining elements after merge loop
  - Overwriting the entire array instead of only `arr[l..r]`
- **Quick Sort**
  - Confusion between partition logic and recursion logic
  - Not clearly fixing the pivot before recursive calls
  - Misunderstanding base case (`l >= r`)
  - Difficulty tracing pointer movement during partition

## Anchor Problems
- Generate Binary Strings with wildcards (`?`)
- Letter Case Permutation / Subsets generation
- Merge Sort (classic divide & conquer)
- Quick Sort (partition-based recursion)
- Array sorting and recursion fundamentals
