# **Recurrence Relation: T(n) = 2T(n/2) + n | Substitution Method**

## **📌 Introduction**
A **recurrence relation** is a mathematical formula that defines a function in terms of its smaller input values. In this lecture, we analyze and solve the recurrence:

\[ T(n) = 2T(n/2) + n \]

where:
- \( T(n) \) represents the time complexity of solving a problem of size \( n \).
- \( T(n/2) \) represents solving two subproblems of size \( n/2 \).
- \( n \) represents the additional work done at each level of recursion.

## **🔍 Solving Using Substitution Method**
We apply the **Substitution Method** to expand the recurrence step by step:

### **Step 1: Expand the Recurrence**
Expanding the recurrence for the first few steps:
1. **First expansion:**
   \[ T(n) = 2T(n/2) + n \]
2. **Expand \( T(n/2) \):**
   \[ T(n) = 2(2T(n/4) + n/2) + n \]
   \[ T(n) = 4T(n/4) + 2(n/2) + n \]
   \[ T(n) = 4T(n/4) + n + n \]
3. **Expand \( T(n/4) \):**
   \[ T(n) = 4(2T(n/8) + n/4) + 2n \]
   \[ T(n) = 8T(n/8) + n + n + n \]
4. **Generalizing for \( k \) expansions:**
   \[ T(n) = 2^k T(n/2^k) + k n \]

### **Step 2: Identify the Base Case**
- The recurrence keeps breaking down until \( n/2^k = 1 \), meaning \( k = \log_2 n \).
- When \( n/2^k = 1 \), we have:
  \[ T(1) = O(1) \]
- Substituting \( k = \log_2 n \):
  \[ T(n) = 2^{\log_2 n} T(1) + n \log_2 n \]
  \[ T(n) = n T(1) + n \log_2 n \]
  \[ T(n) = O(n \log n) \]

## **📊 Graphical Representation**
```
T(n) = 2T(n/2) + n

        T(n)
       /   \
  T(n/2)  T(n/2)
   / \      / \
T(n/4) T(n/4) T(n/4) T(n/4)
```
- The tree has **log n** levels.
- The total work done at each level is proportional to **n**.
- The total complexity sums to **O(n log n)**.

## **📌 Conclusion**
- The recurrence \( T(n) = 2T(n/2) + n \) describes **Divide and Conquer Recurrences**.
- Solving it using the **Substitution Method** gives a time complexity of **O(n log n)**.
- This confirms that many efficient algorithms, like **Merge Sort**, operate in **O(n log n)** time.

---
📌 **Mastering recurrence relations is key to understanding algorithm efficiency! Keep practicing! 🚀**
