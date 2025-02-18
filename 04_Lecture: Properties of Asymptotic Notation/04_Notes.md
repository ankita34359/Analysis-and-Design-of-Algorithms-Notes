# **Properties of Asymptotic Notation**

### **Introduction**
Asymptotic notation helps in analyzing an algorithm’s efficiency. It follows specific mathematical properties that allow better comparison and simplification of time complexity expressions.

It help in analyzing the efficiency of algorithms. These notations have specific mathematical properties:
1. **Symmetric Property**
2. **Reflexive Property**
3. **Transitive Property**

### **Properties of Different Asymptotic Notations**
We will analyze these properties for **Big O (O), Big Omega (Ω), Big Theta (Θ), Small o (o), and Small Omega (ω).**

#### **1. Symmetric Property**
- A relation **R** is symmetric if:
  \[ f(n) R g(n) => g(n) R f(n) \]
- **Applies to:** Θ (Theta)
- **Does not apply to:** O, Ω, o, ω

#### **2. Reflexive Property**
- A relation **R** is reflexive if:
  \[ f(n) R f(n) \]
- **Applies to:** O, Ω, Θ
- **Does not apply to:** o, ω

#### **3. Transitive Property**
- A relation **R** is transitive if:
  \[ f(n) R g(n) \text{ and } g(n) R h(n) \Rightarrow f(n) R h(n) \]
- **Applies to:** O, Ω, Θ, o, ω

### **Comparison Table**
| Property  | Big O (O) | Big Omega (Ω) | Big Theta (Θ) | Small o (o) | Small Omega (ω) |
|-----------|----------|--------------|--------------|------------|---------------|
| Symmetric | ❌       | ❌           | ✅           | ❌         | ❌           |
| Reflexive | ✅       | ✅           | ✅           | ❌         | ❌           |
| Transitive | ✅      | ✅           | ✅           | ✅         | ✅           |

### **Explanation with Examples**
#### **1. Symmetric Property Example**
- **Θ(n²) is symmetric:** If **f(n) = Θ(g(n))**, then **g(n) = Θ(f(n))**.
- **O(n²) is not symmetric:** If **f(n) = O(g(n))**, it does not imply **g(n) = O(f(n))**.

#### **2. Reflexive Property Example**
- **O(n²) is reflexive:** Any function **f(n) = O(f(n))**.
- **o(n²) is not reflexive:** **o(n²)** means **f(n) grows strictly slower than n²**, so it does not hold for itself.

#### **3. Transitive Property Example**
- If **f(n) = O(g(n))** and **g(n) = O(h(n))**, then **f(n) = O(h(n))**.

**Diagram:**
```
   O(f(n)) + O(g(n)) = O(max(f(n), g(n)))
   O(f(n)) * O(g(n)) = O(f(n) * g(n))
```

### **Comparison between Functions (Fn and gn)**
- If **f(n) = O(g(n))**, then **f(n)** grows at most as fast as **g(n)**.
- If **f(n) = Ω(g(n))**, then **f(n)** grows at least as fast as **g(n)**.
- If **f(n) = Θ(g(n))**, then **f(n)** and **g(n)** grow at the same rate.

**Diagram:**
```
   f(n) = O(g(n))   → Upper Bound
   f(n) = Ω(g(n))   → Lower Bound
   f(n) = Θ(g(n))   → Tight Bound
```

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

**Diagram:**
```
   n log n → O(n log n)
   n²      → O(n²)
   n³      → O(n³)
```
### **Importance of These Properties**
- Helps in simplifying complex time complexity expressions.
- Allows accurate classification of algorithm efficiency.
- Aids in comparing multiple algorithms effectively.

**Diagram:**
```
   O(g(n))
      |
      |------> Growth of f(n)
      |
   Ω(g(n))
```

### **Conclusion**
Understanding these properties helps in proving relationships between different functions, making asymptotic analysis more rigorous.

