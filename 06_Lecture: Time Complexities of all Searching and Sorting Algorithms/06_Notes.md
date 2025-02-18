# **Time Complexities of Searching and Sorting Algorithms**

### **Introduction**
Understanding the time complexities of searching and sorting algorithms is crucial for selecting the most efficient algorithm based on problem constraints and input size.

### **Time Complexities of Searching Algorithms**
1. **Linear Search**: O(n)
   - Checks each element one by one.
   - Inefficient for large datasets.

2. **Binary Search**: O(log n)
   - Works on sorted arrays.
   - Repeatedly divides the search range in half.

### **Time Complexities of Sorting Algorithms**
1. **Bubble Sort, Selection Sort, Insertion Sort**: O(n²)
   - Simple but inefficient for large inputs.
   - **Best Case (Insertion Sort)**: O(n) when the array is already sorted.

2. **Merge Sort, Quick Sort, Heap Sort**: O(n log n)
   - Efficient and commonly used.
   - Merge Sort has consistent O(n log n) complexity.
   - Quick Sort can degrade to O(n²) in the worst case.

3. **Heap Sort**: O(n log n)
   - Uses a binary heap data structure.
   - **Heap Construction**: O(n log n)
   - **Heap Deletion**: O(log n)

4. **Counting Sort, Radix Sort, Bucket Sort**: O(n)
   - Work efficiently for limited value ranges.
   
### **Complexities of Graph Algorithms Related to Sorting**
1. **Huffman Coding**: O(n log n)
2. **Prim’s Algorithm**: O(n log n)
3. **Kruskal’s Algorithm**: O(n log n)

### **Conclusion**
- **Sorting algorithms** with O(n log n) complexity are generally more efficient for large datasets.
- **Searching algorithms** like binary search significantly reduce time complexity when working with sorted data.
- **Understanding these complexities helps optimize algorithm selection for real-world applications.**


