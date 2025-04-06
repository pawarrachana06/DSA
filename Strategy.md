# 🚀 Coding Strategies & Patterns Guide (A to Z for Beginners)

This guide is your go-to resource for learning how to solve coding problems like a pro — even if you're just starting out. Each strategy includes a basic explanation, common patterns, and time complexities.

---

## 1. 🟨 Two Pointers

**Use When:** Working with sorted arrays, string problems, or when you need to compare elements or move inwards/outwards.

### 🔹 Patterns:
- Opposite ends (e.g., check palindrome)
- Same direction (slow-fast)
- Remove duplicates

### ⏱ Time Complexity:
- Typically **O(n)**

### ✅ Examples:
- Reverse String
- Remove Duplicates from Sorted Array
- Container With Most Water

---

## 2. 🟦 Sliding Window

**Use When:** You're asked for the max/min/sum/length of a subarray or substring.

### 🔹 Patterns:
- Fixed window size
- Dynamic window size (expand/shrink)

### ⏱ Time Complexity:
- Typically **O(n)**

### ✅ Examples:
- Maximum Subarray Sum
- Longest Substring Without Repeating Characters
- Minimum Window Substring

---

## 3. 🟩 Hashing (HashMap/Set)

**Use When:** Need fast lookup, to store frequency, or avoid duplicates.

### 🔹 Patterns:
- Count occurrences
- Check for existence
- Store indices or seen elements

### ⏱ Time Complexity:
- Lookup: **O(1)** average (HashMap)

### ✅ Examples:
- Two Sum
- Group Anagrams
- Longest Consecutive Sequence

---

## 4. 🟧 Binary Search

**Use When:** Array is sorted or when searching for a number, position, or condition that follows a pattern.

### 🔹 Patterns:
- Classic binary search
- Lower/Upper bound
- Binary search on answer (min/max)

### ⏱ Time Complexity:
- **O(log n)**

### ✅ Examples:
- Search in Rotated Sorted Array
- Find First and Last Position
- Peak Element

---

## 5. 🟪 Greedy

**Use When:** Want optimal solution using locally best choice at each step (without backtracking).

### 🔹 Patterns:
- Sort + pick greedily
- Interval merging

### ⏱ Time Complexity:
- Depends, typically **O(n log n)** due to sorting

### ✅ Examples:
- Jump Game
- Merge Intervals
- Activity Selection

---

## 6. 🟥 Dynamic Programming (DP)

**Use When:** Problem has overlapping subproblems and optimal substructure.

### 🔹 Patterns:
- Memoization (top-down)
- Tabulation (bottom-up)
- 1D or 2D DP arrays

### ⏱ Time Complexity:
- Varies, often **O(n)** to **O(n^2)** or **O(n * m)**

### ✅ Examples:
- Climbing Stairs
- Longest Increasing Subsequence
- 0/1 Knapsack

---

## 7. 🟫 Backtracking

**Use When:** Need to explore all combinations, permutations, or possibilities.

### 🔹 Patterns:
- Recursion with pruning
- Try + undo (DFS-style)

### ⏱ Time Complexity:
- **O(2^n)** or worse

### ✅ Examples:
- N-Queens
- Sudoku Solver
- Subsets and Permutations

---

## 8. ⚪️ Union-Find (Disjoint Set)

**Use When:** Graph connectivity problems (connected components, cycles).

### 🔹 Patterns:
- Union by rank
- Path compression

### ⏱ Time Complexity:
- Almost constant: **O(α(n))**, where α is inverse Ackermann

### ✅ Examples:
- Friend Circles
- Redundant Connection
- Kruskal’s Algorithm

---

## 9. 🔷 Graph Traversal (BFS/DFS)

**Use When:** Problems on grids, shortest paths, islands, graphs.

### 🔹 Patterns:
- Recursive DFS
- Queue-based BFS
- Level-order traversal

### ⏱ Time Complexity:
- **O(V + E)** for graphs

### ✅ Examples:
- Number of Islands
- Word Ladder
- Rotting Oranges

---

## 10. 🧩 Heap / Priority Queue

**Use When:** You need to always get the min/max element efficiently.

### 🔹 Patterns:
- Maintain top `k`
- Custom comparator

### ⏱ Time Complexity:
- Insert/delete: **O(log n)**

### ✅ Examples:
- Kth Largest Element
- Top K Frequent Elements
- Merge K Sorted Lists

---

## 📌 Bonus: Strategy vs Data Structure

- **Strategy** = *How* you approach the problem (e.g., sliding window)
- **Data Structure** = *What* you use to store/manipulate data (e.g., hash map, heap)

---

## 🧠 Want to Practice?
Use this list as a **checklist**: Try 2 problems from each category.

> Ask yourself: "Which strategy fits this problem?"

---

Now you're ready to code smarter, not just harder 💡

