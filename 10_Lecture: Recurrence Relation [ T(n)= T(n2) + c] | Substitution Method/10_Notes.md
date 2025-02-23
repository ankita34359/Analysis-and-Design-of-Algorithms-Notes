# **Recurrence Relation: T(n) = T(n/2) + c | Substitution Method** 

## **📌 Introduction**
Recurrence relations are used to express the running time of recursive algorithms. In this lecture, we analyze the recurrence relation for **Binary Search**:

\[ T(n) = T(n/2) + c \]

where:
- \(T(n)\) represents the time complexity of solving a problem of size \(n\)
- \(T(n/2)\) represents the time complexity of solving a smaller subproblem of size \(n/2\)
- \(c\) is a constant time taken for computing the middle element and making comparisons.

## **Substitution Method Analysis**
We apply the **Substitution Method** to solve the recurrence:

1. **Expand the recurrence step by step:**
   - \( T(n) = T(n/2) + c \)
   - \( T(n/2) = T(n/4) + c \)
   - \( T(n/4) = T(n/8) + c \)
   - Generalizing:
     \[ T(n) = T(n/2^k) + k*c \]

2. **Determine the stopping condition:**
   - The recurrence continues until \( n/2^k = 1 \), i.e., \( k = log_2{n} \)

3. **Substituting \( k \) into the equation:**
   \[ T(n) = T(1) + c*log_2{n} \]

4. **Final Complexity:**
   - Since \( T(1) \) is a constant, we get:
     \[ T(n) = O(\log n) \]

## **Graphical Representation**
```
T(n) = T(n/2) + c

     n
    / \
  n/2  c
 /  \
...  ...
```
- The number of levels in the recursion tree is \ (log_2{n} \)
- At each level, we perform constant work \( c \)
- The total complexity sums up to **O(log n)**

## **📌 Conclusion**
- The recurrence relation \( T(n) = T(n/2) + c \) describes **Binary Search**.
- Solving it using the **Substitution Method** gives us a time complexity of **O(log n)**.
- This confirms that **Binary Search is highly efficient** compared to linear search (**O(n)**).

---
📌 **Keep practicing and analyzing different recurrence relations for a deeper understanding!** 🚀


