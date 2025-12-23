# Two Pointers Pattern⚡

### What it is:
*Use two indices instead of one to process an array or string more efficiently.*

A technique where two variables(pointers) traverse a data structure (like an array, string, or linked list) simultaneously from different positions.

*two pointers either move towards each other, away from each other, or in the same direction.*


### When to think of Two Pointers?
    The moment you see:
    
    -Sorted array / string
    -Pairs / comparison between elements
    -Left vs right
    -“Find / remove / reverse / check” type problems
        Your brain should go: “Two pointers?” 👀

### How it works (mentally)
    i. Put one pointer at start
    ii. Put one pointer at end (or both at start)
    iii. Move pointers based on condition
    iv. Stop when they meet or cross
  
    That’s it. 

### Common pointer styles
    
    (a) Opposite direction
      left → ← right
      Used in: reverse array, pair sum in sorted array
    
    (b) Same direction
      slow → fast →
      Used in: remove duplicates, move zeros

### Why interviewers love it
    -Converts O(n²) brute force → O(n)
    -Shows optimization thinking
    -Saves space (often O(1))

### One-line memory hook 🧠

    “If I’m comparing elements or shrinking a range — two pointers can probably do it.”

### Classic examples

    Reverse a string
    
    Check palindrome
    
    Pair with target sum (sorted array)
    
    Remove duplicates in-place

## Strict warning 😤

    If the array is not sorted,
    Two Pointers usually won’t work (unless you sort first).
