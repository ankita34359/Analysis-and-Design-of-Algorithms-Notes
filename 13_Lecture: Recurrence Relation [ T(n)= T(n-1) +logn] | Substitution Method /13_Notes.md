# **Recurrence Relation: T(n) = T(n-1) + log n | Substitution Method**

## **Introduction**
A **recurrence relation** defines a function based on its values at smaller inputs. In this lecture, we analyze and solve the recurrence:

\[ T(n) = T(n-1) + \log n \]

where:
- \( T(n) \) represents the time complexity of solving a problem of size \( n \).
- \( T(n-1) \) represents solving a subproblem of size \( n-1 \).
- \( \log n \) represents the additional work done at each step.

## **Solving Using Substitution Method**
We solve the recurrence step by step:

### **Step 1: Expand the Recurrence**
Expanding for the first few steps:
1. **First expansion:**
   \[ T(n) = T(n-1) + log n \]
2. **Expand \( T(n-1) \):**
   \[ T(n) = (T(n-2) + \log (n-1)) + \log n \]
   \[ T(n) = T(n-2) + \log(n-1) + \log n \]
3. **Expand \( T(n-2) \):**
   \[ T(n) = T(n-3) + \log(n-2) + \log(n-1) + \log n \]
4. **Generalizing for \( k \) expansions:**
   \[ T(n) = T(n-k) + \sum_{i=n-k+1}^{n} \log i \]

### **Step 2: Identify the Base Case**
- The recurrence keeps breaking down until \( n-k = 1 \), meaning \( k = n-1 \).
- When \( T(1) = O(1) \), we get:
  \[ T(n) = O(1) + \sum_{i=2}^{n} \log i \]

### **Step 3: Solve the Summation**
The sum \( \sum_{i=2}^{n} \log i \) is equivalent to:
\[ \log(2) + \log(3) + \log(4) + ... + \log(n) \]
Using logarithm properties, we rewrite it as:
\[ \log(2 \times 3 \times 4 \times ... \times n) = \log(n!) \]
Using **Stirling's approximation**:  \( \log(n!) \approx n \log n - n \), we approximate:
\[ T(n) = O(n \log n) \]

## **Graphical Representation**
```
T(n) = T(n-1) + log n

        T(n)
        |
      T(n-1)  + log n
       |
     T(n-2)  + log(n-1)
       |
    T(n-3)  + log(n-2)
```
- The recurrence decreases **linearly**.
- The total work done sums to **O(n log n)**.

## **Conclusion**
- The recurrence \( T(n) = T(n-1) + \log n \) describes a **logarithmic increment** at each level.
- Solving it using the **Substitution Method** gives a time complexity of **O(n log n)**.
- This complexity is often seen in algorithms that incrementally process logarithmic amounts of work.

---
**Understanding recurrence relations is crucial for algorithm analysis! Keep practicing! 🚀**


