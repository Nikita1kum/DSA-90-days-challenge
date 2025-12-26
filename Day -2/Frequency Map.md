# 📌 Frequency Map / Frequency Array (DSA Pattern)

## 1. What is a Frequency Map?

A **Frequency Map** is a technique used to count how many times each element appears in a collection (array, string, etc.).

In simple words:
> It stores  
> **element → number of occurrences**

This avoids repeated counting and helps solve problems efficiently.

---

## 2. Example

### Input
"mississippi"

### Frequency Result

    m → 1
    i → 4
    s → 4
    p → 2

Instead of scanning the string again and again, we count once and reuse the information.

---

## 3. Frequency Array vs Frequency Map

### 🔹 Frequency Array

Use when:
- Input range is **fixed and small**
- Examples: lowercase letters (`a–z`), digits (`0–9`)
      
      int freq[26] = {0};
      
      for(char ch : s) {
          freq[ch - 'a']++;
      }

##### Pros

    Very fast
    
    Less memory overhead
    
##### Cons

    Limited to known ranges

### 🔹 Frequency Map (HashMap)

Use when:

- Input range is large or unknown

Examples: integers, large values, characters beyond a–z

    unordered_map<int, int> freq;
    
    for(int x : nums) {
        freq[x]++;
    }

##### Pros

    Flexible
    
    Works for any data type
    
##### Cons

    Slightly slower than array

### 4. Pattern Skeleton (Template)
##### Step 1: Collect information
    for(element in input) {
        freq[element]++;
    }

##### Step 2: Use information

    compare frequencies
    
    validate conditions
    
    find max / min frequency
    
    construct the answer

- This two-phase structure is the core of the pattern.

### 5. Time and Space Complexity
    Operation  	Complexity
    Build       frequency	O(n)
    Lookup	    O(1)
    Iterate     frequency	O(k)
    Space	      O(k)

Where:

n = input size

k = number of unique elements
