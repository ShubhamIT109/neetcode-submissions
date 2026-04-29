# DSA Grind Log

## Day 1 - April 19, 2026
- Solved: Two Sum, Contains Duplicate
- Learnt: HashMap complement pattern, HashSet duplicate check
- Struggled with: HashMap and HashSet methods like containsKey, put,contains,add
- also find bit difficulty with array syntax 


## Day 2 - April 20, 2026

- Solved: Valid Anagram (LC 242)

Learnt:

* Frequency counting using HashMap and array
* +1 for first string and -1 for second string approach
* Early detection using negative frequency
* Difference between HashMap vs array[26] optimization

Struggled with:

* Correct use of HashMap methods (getOrDefault, containsKey)
* Updating frequency for correct character (mixing s and t indices)
* Where to check negative condition (before vs after decrement)
* Thinking about final validation vs early return logic

## Day 4 - April 29, 2026

Date: 29 April 2026  
Problem: Product of Array Except Self (LC #238)  
Difficulty: Medium  
Status: ✅ Solved Independently  
(Previously attempted on 28 April — struggled with implementation)

---

### Approach:
- prefix[i] = product of all elements to LEFT of i
- suffix[i] = product of all elements to RIGHT of i
- ans[i] = prefix[i] * suffix[i]
- Base values: prefix[0] = 1, suffix[n-1] = 1

---

### Pattern:
Prefix-Suffix Array  

Use this when:
Answer at each index depends on elements before AND after it

---

### Complexity:
- TC: O(n) — three passes
- SC: O(n) — prefix + suffix arrays

---

### Dry Run:
nums   = [1,  2,  3,  4]  
prefix = [1,  1,  2,  6]  
suffix = [24, 12, 4,  1]  
ans    = [24, 12, 8,  6]

---

### Key Insight:
- Product of "nothing" = 1 (not 0)
- Always initialize boundary values to 1 in prefix/suffix problems

---

### What Improved Today:
- Successfully implemented full logic without bugs
- Correctly handled boundary cases (i=0 and i=n-1)
- Clear understanding of prefix-suffix pattern

---

### Previous Mistakes (Fixed):
- Confusion between enhanced for loop and index-based loop
- Forgot boundary initialization
- ArrayIndexOutOfBounds at i=0

---

### Java Rules Reinforced:
- for(int x : arr) → value (read-only)
- for(int i=0;i<n;i++) → use for index operations
- Never access prefix[-1] → handle edges explicitly

---

### Revisit Dates:
2 May | 6 May | 13 May  

⚠️ Status Upgrade: From "Struggled" → "Independent Solve"
