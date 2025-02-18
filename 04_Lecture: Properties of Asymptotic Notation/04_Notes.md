**Properties of Asymptotic Notation**

### **Introduction**
Asymptotic notation helps in analyzing an algorithm’s efficiency. It follows specific mathematical properties that allow better comparison and simplification of time complexity expressions.

### **Comparison between Functions (Fn and gn)**
- If **f(n) = O(g(n))**, then **f(n)** grows at most as fast as **g(n)**.
- If **f(n) = Ω(g(n))**, then **f(n)** grows at least as fast as **g(n)**.
- If **f(n) = Θ(g(n))**, then **f(n)** and **g(n)** grow at the same rate.

### **Comparison of Various Asymptotic Notations**
- **Big O (O)**: Upper bound (worst-case complexity)
- **Big Omega (Ω)**: Lower bound (best-case complexity)
- **Big Theta (Θ)**: Tight bound (average-case complexity)

### **Difference Between Big O and Big Omega**
- **Big O (O)**: Represents the maximum growth rate.
- **Big Omega (Ω)**: Represents the minimum growth rate.
- **Example:** If **f(n) = 3n² + 2n + 5**, then:
  - **O(n²)** → Upper bound
  - **Ω(n²)** → Lower bound
  - **Θ(n²)** → Tight bound (if upper and lower bounds match)

### **Key Properties of Asymptotic Notation**
1. **Transitivity**: If **f(n) = O(g(n))** and **g(n) = O(h(n))**, then **f(n) = O(h(n))**.
2. **Reflexivity**: **f(n) = O(f(n))**, **f(n) = Ω(f(n))**, **f(n) = Θ(f(n))**.
3. **Symmetry in Theta**: If **f(n) = Θ(g(n))**, then **g(n) = Θ(f(n))**.
4. **Addition Rule**: If **f(n) = O(g(n))** and **h(n) = O(g(n))**, then **(f(n) + h(n)) = O(g(n))**.
5. **Multiplication Rule**: If **f(n) = O(g(n))** and **h(n) = O(k(n))**, then **(f(n) * h(n)) = O(g(n) * k(n))**.

### **Importance of These Properties**
- Helps in simplifying complex time complexity expressions.
- Allows accurate classification of algorithm efficiency.
- Aids in comparing multiple algorithms effectively.

Understanding these properties enables efficient problem-solving and better selection of optimal algorithms.


