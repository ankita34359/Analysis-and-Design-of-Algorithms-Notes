# **Recurrence Relation & Binary Search Recurrence Relation**    
 
### **Introduction**
A **Recurrence Relation** is a mathematical function that defines a sequence recursively by expressing each term as a function of its preceding terms.

### **Understanding Recurrence Relation**
- Recurrence relations occur in algorithms where a problem is broken into smaller subproblems.
- Example: Binary Search, Merge Sort, Fibonacci sequence.
- They can be solved using:
  
  1. **Substitution Method**
  2. **Master Theorem**
  3. **Recursion Tree Method**

### **Binary Search & Its Recurrence Relation**
Binary Search is an efficient algorithm for searching an element in a **sorted array** by repeatedly dividing the search space in half.

#### **Steps in Binary Search**
1. Find the **middle element** of the array.
2. Compare the middle element with the target:
   - If equal, return the index.
   - If target is smaller, search in the left half.
   - If target is larger, search in the right half.
3. Repeat until the element is found or the search space is empty.

#### **Recurrence Relation for Binary Search**
- Binary Search divides the array into two parts in each step.
- The recurrence relation is:
  
  **T(n) = T(n/2) + O(1)**
  
  Where:
  - **T(n)** represents the time complexity for an array of size **n**.
  - **T(n/2)** represents the recursive call on half the array.
  - **O(1)** accounts for calculating the middle element and comparing it.

**Diagram Representation:**
```
          n  (Original Array)
         / \
    n/2    n/2  (Divided Halves)
    /  \   /  \
n/4  n/4 n/4 n/4 (Further Division)
```

### **Solving the Recurrence Relation**
1. **Substitution Method**
   - Expand the recurrence relation step by step.
   - Keep expanding until reaching the base case **T(1) = O(1)**.
   - Results in **O(log n)** complexity.

2. **Master Theorem**
   - The recurrence follows the form **T(n) = T(n/b) + O(f(n))**.
   - Here, **a = 1, b = 2, f(n) = O(1)**.
   - Applying Master Theorem, **O(log n)** is derived.

3. **Recursion Tree Method**
   - Visualizing recursion as a tree where each level reduces the problem size.
   - The depth of the tree is **log n**, resulting in **O(log n)** complexity.

### **Conclusion**
- **Binary Search** follows a recurrence relation of **T(n) = T(n/2) + O(1)**.
- The time complexity is **O(log n)**.
- Understanding recurrence relations helps in analyzing recursive algorithms efficiently.

**Key Takeaway:** Recurrence relations play a crucial role in defining and solving problems in computer science, making them an essential topic for algorithm analysis.


