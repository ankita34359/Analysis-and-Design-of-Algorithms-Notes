# **Recurrence Relation: T(n) = n * T(n-1) | Substitution Method**

## **📌 Introduction**
A **recurrence relation** is a mathematical equation that defines a sequence based on previous terms. In this lecture, we analyze the recurrence relation:

\[ T(n) = n \times T(n-1) \]

where:
- \( T(n) \) represents the time complexity of solving a problem of size \( n \).
- \( T(n-1) \) represents the time complexity of solving a smaller subproblem of size \( n-1 \).
- \( n \) is the additional work done at each step.

## **🔍 Solving Using Substitution Method**
We apply the **Substitution Method** to solve this recurrence:

1. **Expand the recurrence step by step:**
   - \( T(n) = nxT(n-1) \)
   - \( T(n-1) = (n-1)xT(n-2) \)
   - \( T(n-2) = (n-2)xT(n-3) \)
   - Expanding further:
     \[ T(n) = nx(n-1)x(n-2)x(n-3)x ... x2x1xT(1) \]

2. **Determine the base case:**
   - If \( T(1) = 1 \), then we get:
     \[ T(n) = n! \]

3. **Detailed Step-by-Step Calculation:**
   - Let's compute for small values of \( n \):
     - \( T(1) = 1 \)
     - \( T(2) = 2xT(1) = 2x1 = 2 \)
     - \( T(3) = 3xT(2) = 3x2 = 6 \)
     - \( T(4) = 4xT(3) = 4x6 = 24 \)
     - \( T(5) = 5xT(4) = 5x24 = 120 \)
   - As seen from the calculations, the values grow extremely fast.

4. **Final Complexity:**
   - Since factorial growth is extremely fast, we conclude:
     \[ T(n) = O(n!) \]

## **📊 Graphical Representation**
```
T(n) = n * T(n-1)

     n
    / \
  n-1  n
 /  \
...  ...
```
- Each level multiplies the previous result by an additional factor.
- The number of levels in the recursion tree is **n**, leading to **O(n!)** complexity.

## **📌 Conclusion**
- The recurrence relation \( T(n) = n \times T(n-1) \) describes **Factorial Growth**.
- Solving it using the **Substitution Method** gives us a time complexity of **O(n!)**.
- This confirms that **Factorial Time Complexity** is extremely inefficient for large inputs.
- Factorial growth is much slower than polynomial or exponential complexities, making such algorithms impractical for large inputs.

---
📌 **Understanding recurrence relations is crucial for mastering algorithm analysis! Keep practicing!** 🚀


