# DSA ALGORITHM

## TIME AND SPACE COMPLEXITY

#### TIME COMPLEXITY

Not the actual time taken to run the program on machine (Its not machine dependent as the program might take different time on diffrent OS or platform eg Leetcode server based).It is the amout of time taken as function of input size(n)

No of operation changes as n increases.
NOTE: we consider worst case , since if x algorithm works with 10T users perfectly , certainly it will work for 10 users.

#### SPACE COMPLEXITY
Amout of space taken by an algorithm as function of input size (n)

code : 
1. Input space (vector, array , string)

2. Auxiliary space ( extra space )

We consider only auxiliary space
       


#### BIG 0 NOTATION

The symbol we give for a number , displays its power 
eg: $5 and ₹5 

Different notations

1. Big O (worst case/upper bound)  (Consider the highest term) eg n^2 +n+5 =O(n^2)

2. Theta (θ)  Average case

3. Omega (Ω) (lower bound / best case)

#### BEST TO WORST TIME COMPLEXITY   

![image](https://github.com/user-attachments/assets/af101c7a-16a1-42a0-9da1-17b0f48382f7)

eg: sum of numbers from 1 to N

1. O(1) : No matter the n is large or small , same No of operation  will be performed.



``` Cpp
int n;
cin >> n;
int ans =n *(n+1)/3

```

2. O(n)

factorial sort
``` cpp
int fact=1;
for(int i=1;i<=n;i++){
fact*=i;
}
```

3. O(n^2) & O(n^3)

bubble sort
``` cpp
for (int i=0;i<n-1;i++){
for(int j=0;j<n-i-1;j++){
if(arr[j] > arr[j+1]) {
swap(arr[j],arr[j+1]);
}
}
}

```


4 . O(log n)
Binary search /BST

``` cpp
int s=0,e=n-1;
while(s<=e){

int mid=s+(e-s)/2;
if(arr[mid]<target){
s=mid+1;
}
else if(arr[mid]>target){
e=mid+1;
}
else{
return mid;}
}


```

5. O(nlogn)
 sorting
merge sort

6. O(2^n) & O(n!) (Worst than O(2^n)
 Recursion

### PROBLEMS 

1. Prime numbers

``` cpp
for(int i=2;i*i<= n;i++)
{
if(n%i ==0)
{
cout << "Non prime"
break;
}
}
```

Time complexity : O(√n)
the loop will run till i^2=n --> i=√n

O(√n) < O(n)

2. Selection sort

``` cpp

for(int i=0;i<n-1;i++)
{
int minIdx=i;
for (int j=i+1;j<n;j++)
{
if(arr[j]<arr[minIdx])
{
minIdx=j;
}
}

swap(arr[i],arr[minIdx]);

}

```

Time complexity = n *n =O(n^2)
  
3. Recursion

``` cpp

int factorial(int n)
{

if(n==0)
{
return 1
}
return n*factorial (n-1)

}
```

Time complexity methods

1.Recurrence relation
f(n)=k+f(n-1)=O(n)

![image](https://github.com/user-attachments/assets/e898df43-09fe-4632-9efb-1d0dcad7ba99)


2. Total No of recursion call * work done in each call

![image](https://github.com/user-attachments/assets/f679e9a5-8146-47d0-9746-398800d376bd)


space complexity 

stack occupies memory

SC= height of call stack * memory in each call
SC=O(n)
![image](https://github.com/user-attachments/assets/31404fdb-9c70-449a-93f0-be8ef7a3773f)


4. Recusrsive Fibonacci

``` cpp

int fib(int n)

{

if(n==0 || n==1)
{
return n;
}
return fib(n-1) * (n-2);
}

```
Time complexity:  O(2 ^n)


Space complexity : O(n)
![image](https://github.com/user-attachments/assets/61e73119-6015-484b-86c5-b1aa05b2c737)


![image](https://github.com/user-attachments/assets/b3589dfe-073c-4011-a6b0-47351ae6426e)

5. Merge sort

``` cpp

void mergrSort(int arr[],int si,int ei){

if(si>=ei)
{
return;
}
int mid=si+(ei-si)/2;
mergeSort(arr,si,mid);
mergeSort(arr,mid+1,ei);
merge(arr,si,mid,ei)
}

```

merge : TC O(n)  SC O(n)
![image](https://github.com/user-attachments/assets/b2fcc263-0341-4dbe-8264-b89bbbc4bfe8)

![image](https://github.com/user-attachments/assets/e31f7246-07e7-473a-b282-8cf781c64bad)

merge sort : TC o(n log n) SC 
![image](https://github.com/user-attachments/assets/9288559c-1d89-4044-aeea-3cef5cf32722)

![image](https://github.com/user-attachments/assets/69137881-767e-4bef-b94c-45f9013f491e)

### Code POV

![image](https://github.com/user-attachments/assets/2267f1c3-0f26-4014-9476-5100c74f71b5)

#### ! MOST IMPORTANT
![image](https://github.com/user-attachments/assets/c1af6b5d-0fca-4719-9a07-482b7cc818a8)


# Algorithm Time Complexity Table

This table helps to decide the best algorithm based on the size of input \( n \). The suggested time complexities are the **upper bounds** that should be targeted for efficient execution.

| **Constraint (n ≤ ...)** | **Best Time Complexity** | **Algorithm to Think Of** | **Additional Hints and Algorithms** |
|--------------------------|--------------------------|---------------------------|-------------------------------------|
| \( n > 10^8 \)            | O(log n), O(1)           | Binary Search, Hashing     | Use **hash maps** for constant time lookups and **binary search** to divide and conquer large data. |
| \( n \leq 10^8 \)         | O(n)                     | Prefix Sum, Sliding Window | **Prefix sum** for range queries; **sliding window** for problems involving subarrays or substrings. |
| \( n \leq 10^6 \)         | O(n log n)               | Merge Sort, QuickSort, Dijkstra | Sorting algorithms (**QuickSort**, **MergeSort**) and graph algorithms (**Dijkstra**) are efficient for up to 1 million elements. |
| \( n \leq 10^4 \)         | O(n²)                     | DP (Floyd-Warshall, LIS), Brute Force | Dynamic Programming (**Floyd-Warshall** for shortest paths, **LIS** for longest increasing subsequences), or brute force can work for this range. |
| \( n \leq 500 \)          | O(n³)                     | Matrix Multiplication, DP (Floyd-Warshall) | **Matrix multiplication** and **dynamic programming** algorithms work well for small \( n \). |
| \( n \leq 25 \)           | O(2ⁿ)                     | Recursion, Backtracking, Bitmask DP | **Backtracking** for combinatorial problems, **bitmask DP** for subset problems, and **recursion** for solving smaller subproblems. |
| \( n \leq 12 \)           | O(n!)                     | Permutations, Traveling Salesman Problem | For very small \( n \), **factorial-time algorithms** like solving **permutations** or the **Traveling Salesman Problem** are feasible. |

---

### **Additional Algorithms and Tips**:

- **O(1) Algorithms**: Use when you need constant time operations (e.g., **hashing** for dictionary lookups or **binary search** for sorted arrays).
- **O(n log n)**: Best for **sorting** and **divide-and-conquer** algorithms like **QuickSort**, **MergeSort**, and **HeapSort**.
- **O(n²)**: Suitable for **brute force** or **dynamic programming** solutions when \( n \) is not too large, such as **Floyd-Warshall** for shortest paths in dense graphs.
- **O(n³)**: Works for small \( n \) values, especially in **matrix operations** (e.g., **matrix multiplication**) or **dynamic programming** solutions (e.g., **Floyd-Warshall** for all-pairs shortest paths).
- **O(2ⁿ)**: For small \( n \) problems where you need to explore all subsets, such as **subset sum**, **backtracking**, or **bitmask dynamic programming**.
- **O(n!)**: When \( n \) is very small (e.g., up to 12), **permutations** or **Traveling Salesman Problem (TSP)** can be solved in factorial time.

### **General Guidelines**:
- **For very large data** (\( n > 10^8 \)): Aim for **logarithmic time** or **constant time** solutions (e.g., **binary search**, **hashing**).
- **For medium to large inputs** (\( n \leq 10^6 \)): **Sorting algorithms** and **graph algorithms** (e.g., **Dijkstra**) are usually good choices.
- **For small inputs** (\( n \leq 500 \)): You can afford algorithms with **quadratic** or **cubic time complexity** like **matrix multiplication** or **Floyd-Warshall**.

---

### Conclusion:

- **Use the smallest time complexity** that can still solve the problem efficiently for the given input size \( n \).
- **As the input size increases**, prioritize algorithms that reduce the number of operations, such as **binary search**, **divide-and-conquer**, or **hashing**.
- **For small input sizes**, you can afford to use more exhaustive approaches like **dynamic programming** or **backtracking**.

This table serves as a guide to help you make the best choice for algorithm selection based on input size and time complexity considerations.




# **Basic Data Structures**


![image](https://github.com/user-attachments/assets/e8d7562d-d1cf-4838-88f8-fca8515b8ce4)


# **Linear vs Non-Linear Data Structures**

## **1. Introduction**
Data structures are categorized based on how data elements are organized. The two primary classifications are:
- **Linear Data Structures**: Data elements are arranged sequentially.
- **Non-Linear Data Structures**: Data elements are arranged in a hierarchical or interconnected manner.

---
## **2. Linear Data Structures**
Linear data structures store elements in a sequential order, meaning each element has a direct relationship with its previous and next elements.

### **Characteristics:**
- Elements are stored in a linear sequence.
- Requires more memory as the size grows.
- Easy to implement due to sequential storage.

### **Examples & Time Complexity:**
| Data Structure | Description | Common Operations | Time Complexity |
|---------------|------------|--------------------|-----------------|
| **Array** | Stores elements in contiguous memory locations | Access: O(1), Insertion/Deletion: O(n), Search: O(n) |
| **Linked List** | Elements (nodes) linked with pointers | Access: O(n), Insertion/Deletion: O(1) (at head) |
| **Stack** | Follows LIFO (Last In, First Out) | Push: O(1), Pop: O(1), Peek: O(1) |
| **Queue** | Follows FIFO (First In, First Out) | Enqueue: O(1), Dequeue: O(1) |

### **Example of a Linear Data Structure (Stack in Python)**
```python
class Stack:
    def __init__(self):
        self.stack = []
    
    def push(self, item):
        self.stack.append(item)
    
    def pop(self):
        if not self.is_empty():
            return self.stack.pop()
        return "Stack is empty"
    
    def is_empty(self):
        return len(self.stack) == 0

s = Stack()
s.push(10)
s.push(20)
print(s.pop())  # Output: 20
```

---
## **3. Non-Linear Data Structures**
In non-linear data structures, elements are connected in a hierarchical or complex relationship, meaning they are not sequentially arranged.

### **Characteristics:**
- Elements are connected in a non-sequential manner.
- Efficient in handling complex relationships between data.
- Requires advanced traversal algorithms.

### **Examples & Time Complexity:**
| Data Structure | Description | Common Operations | Time Complexity |
|---------------|------------|--------------------|-----------------|
| **Trees** | A hierarchical structure with parent-child relationships | Access: O(log n), Insertion: O(log n), Deletion: O(log n) (for balanced trees) |
| **Graphs** | A set of nodes (vertices) connected by edges | BFS/DFS Traversal: O(V+E) |
| **Hash Table** | Stores key-value pairs with fast lookups | Access: O(1) (Average), O(n) (Worst case) |

### **Example of a Non-Linear Data Structure (Binary Tree in Python)**
```python
class Node:
    def __init__(self, key):
        self.left = None
        self.right = None
        self.val = key

def inorder_traversal(root):
    if root:
        inorder_traversal(root.left)
        print(root.val, end=" ")
        inorder_traversal(root.right)

root = Node(10)
root.left = Node(5)
root.right = Node(15)
inorder_traversal(root)  # Output: 5 10 15
```

---
## **4. Key Differences Between Linear and Non-Linear Data Structures**

| Feature | Linear Data Structures | Non-Linear Data Structures |
|---------|------------------------|----------------------------|
| **Organization** | Sequential order | Hierarchical or interlinked |
| **Traversal** | One way at a time | Multiple ways |
| **Implementation Complexity** | Simple | Complex |
| **Usage** | Useful for simple applications like stacks, queues | Used for complex data relationships like trees, graphs |

---
## **5. Conclusion**
- **Linear structures** are simple and efficient for sequential operations.
- **Non-linear structures** are better for hierarchical and interconnected data representation.
- Choosing the right data structure depends on the problem at hand, memory constraints, and performance requirements.

Let me know if you need more examples or explanations! 🚀


## **1. Introduction**
Data structures are fundamental to organizing and managing data efficiently. The five main types of basic data structures are:

- **Arrays**
- **Linked Lists**
- **Stacks**
- **Queues**
- **Hash Tables**

Each of these structures has different characteristics, use cases, and advantages.

---

# **Arrays in Python**

## **Introduction**
An **array** is a data structure that stores multiple values of the same type in contiguous memory locations. Unlike Python lists, which can hold multiple data types, arrays ensure type consistency and optimize memory usage.

Python provides arrays through the `array` module and NumPy for advanced operations.

## **Types of Arrays in Python**
1. **Lists (Built-in dynamic arrays)**
2. **Array Module (Fixed-type arrays)**
3. **NumPy Arrays (Multi-dimensional & optimized operations)**

---

## **1. Lists (Dynamic Arrays in Python)**
Python’s built-in lists behave like dynamic arrays, supporting different data types and resizing automatically.

#### **Example:**
```python
arr = [1, 2, 3, 4, 5]  # Creating a list
print(arr[2])  # Accessing an element
arr.append(6)  # Adding an element
print(arr)
```
**Output:**
```
3
[1, 2, 3, 4, 5, 6]
```

#### **Time Complexity (Big-O)**
| Operation  | Complexity |
|------------|------------|
| Accessing an element (`arr[i]`) | O(1) |
| Appending (`append()`) | O(1) (Amortized) |
| Insertion (`insert(i, x)`) | O(n) |
| Deletion (`del arr[i]`) | O(n) |
| Searching (`x in arr`) | O(n) |

---

## **2. Array Module (Fixed-Type Arrays)**
The `array` module provides efficient storage for large data sets with a single data type.

#### **Example:**
```python
import array
arr = array.array('i', [1, 2, 3, 4, 5])  # 'i' stands for integer
print(arr[1])  # Accessing an element
arr.append(6)  # Adding an element
print(arr)
```
**Output:**
```
2
array('i', [1, 2, 3, 4, 5, 6])
```

#### **Big-O Complexity:**
| Operation | Complexity |
|------------|------------|
| Access (`arr[i]`) | O(1) |
| Append (`arr.append(x)`) | O(1) |
| Insert (`arr.insert(i, x)`) | O(n) |
| Remove (`arr.remove(x)`) | O(n) |
| Search (`x in arr`) | O(n) |

---

## **3. NumPy Arrays (Efficient Multi-Dimensional Arrays)**
NumPy provides powerful operations for handling large numerical datasets.

#### **Example:**
```python
import numpy as np
arr = np.array([1, 2, 3, 4, 5])
print(arr[1])  # Accessing an element
arr = np.append(arr, 6)  # Adding an element
print(arr)
```
**Output:**
```
2
[1 2 3 4 5 6]
```

#### **Big-O Complexity:**
| Operation | Complexity |
|------------|------------|
| Access (`arr[i]`) | O(1) |
| Append (`np.append(arr, x)`) | O(n) |
| Insert (`np.insert(arr, i, x)`) | O(n) |
| Delete (`np.delete(arr, i)`) | O(n) |
| Search (`np.where(arr == x)`) | O(n) |

---

## **4. Multi-Dimensional Arrays in Python**
Multi-dimensional arrays store elements in matrix-like structures, commonly used in numerical computing.

### **Using Lists (Nested Lists)**
```python
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]  # 3x3 Matrix
print(matrix[1][2])  # Accessing element at row 1, column 2
```
**Output:**
```
6
```

### **Using NumPy (Optimized for large datasets)**
```python
import numpy as np
matrix = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
print(matrix[1, 2])  # Accessing element at row 1, column 2
```
**Output:**
```
6
```

#### **Big-O Complexity for Multi-Dimensional Arrays**
| Operation | Complexity |
|------------|------------|
| Access (`arr[i][j]`) | O(1) |
| Insert/Delete (`np.insert() / np.delete()`) | O(n) |
| Search (`np.where(arr == x)`) | O(n) |

---

## **Summary**
- Python supports different types of arrays: Lists, `array` module, and NumPy.
- Lists are dynamic but slow; `array` module provides fixed-type arrays.
- NumPy is best for performance-critical applications and multi-dimensional arrays.
- Big-O complexities vary depending on the type of operation performed.

Let me know if you need more examples or explanations! 🚀


# **Linked List in Python**

## **1. Introduction**
A **linked list** is a linear data structure where elements (nodes) are linked using pointers. Unlike arrays, linked lists do not require contiguous memory allocation, making them dynamic in size.

### **Advantages:**
- Efficient insertions and deletions (O(1) at the head).
- No fixed size, unlike arrays.

### **Disadvantages:**
- Slower access time (O(n) vs. O(1) for arrays).
- Uses extra memory for pointers.

---
## **2. Types of Linked Lists**
1. **Singly Linked List**: Each node points to the next node.
2. **Doubly Linked List**: Each node points to both next and previous nodes.
3. **Circular Linked List**: The last node points back to the first node.

---
## **3. Implementation of Linked List in Python**
### **3.1 Singly Linked List**
```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None

    def append(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
            return
        temp = self.head
        while temp.next:
            temp = temp.next
        temp.next = new_node

    def display(self):
        temp = self.head
        while temp:
            print(temp.data, end=" -> ")
            temp = temp.next
        print("None")

# Example Usage
ll = LinkedList()
ll.append(1)
ll.append(2)
ll.append(3)
ll.display()  # Output: 1 -> 2 -> 3 -> None
```

### **Time Complexity:**
| Operation  | Complexity |
|------------|------------|
| Insertion at Head | O(1) |
| Insertion at Tail | O(n) |
| Deletion at Head | O(1) |
| Deletion at Tail | O(n) |
| Searching | O(n) |

---
## **3.2 Doubly Linked List**
```python
class DNode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None

class DoublyLinkedList:
    def __init__(self):
        self.head = None

    def append(self, data):
        new_node = DNode(data)
        if not self.head:
            self.head = new_node
            return
        temp = self.head
        while temp.next:
            temp = temp.next
        temp.next = new_node
        new_node.prev = temp

    def display(self):
        temp = self.head
        while temp:
            print(temp.data, end=" <-> ")
            temp = temp.next
        print("None")

# Example Usage
dll = DoublyLinkedList()
dll.append(1)
dll.append(2)
dll.append(3)
dll.display()  # Output: 1 <-> 2 <-> 3 <-> None
```

---
## **3.3 Circular Linked List**
```python
class CNode:
    def __init__(self, data):
        self.data = data
        self.next = None

class CircularLinkedList:
    def __init__(self):
        self.head = None

    def append(self, data):
        new_node = CNode(data)
        if not self.head:
            self.head = new_node
            new_node.next = self.head
            return
        temp = self.head
        while temp.next != self.head:
            temp = temp.next
        temp.next = new_node
        new_node.next = self.head

    def display(self):
        if not self.head:
            return
        temp = self.head
        while True:
            print(temp.data, end=" -> ")
            temp = temp.next
            if temp == self.head:
                break
        print("(Back to Head)")

# Example Usage
cll = CircularLinkedList()
cll.append(1)
cll.append(2)
cll.append(3)
cll.display()  # Output: 1 -> 2 -> 3 -> (Back to Head)
```

---
## **3. Operations on Linked Lists**

### **1. Insertion in a Linked List**
Insertion can happen in three places:
- **At the beginning** (O(1))
- **At the end** (O(n) for singly, O(1) for doubly)
- **At a specific position** (O(n))

#### **Example: Insert at the Beginning (Singly Linked List)**
```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None

    def insert_at_beginning(self, data):
        new_node = Node(data)
        new_node.next = self.head
        self.head = new_node

    def display(self):
        temp = self.head
        while temp:
            print(temp.data, end=" -> ")
            temp = temp.next
        print("None")

# Usage
ll = LinkedList()
ll.insert_at_beginning(10)
ll.insert_at_beginning(20)
ll.insert_at_beginning(30)
ll.display()
```
**Output:**
```
30 -> 20 -> 10 -> None
```

---
### **2. Deletion in a Linked List**
Deletion can occur at:
- **Beginning** (O(1))
- **End** (O(n) for singly, O(1) for doubly)
- **Specific position** (O(n))

#### **Example: Delete at the Beginning (Singly Linked List)**
```python
class LinkedList:
    def delete_at_beginning(self):
        if self.head is None:
            print("List is empty")
            return
        self.head = self.head.next

# Usage
ll.delete_at_beginning()
ll.display()
```

---
### **3. Traversal in a Linked List**
Traversal means visiting each node in the list.

#### **Example: Traversal (Singly Linked List)**
```python
def traverse(self):
    temp = self.head
    while temp:
        print(temp.data, end=" -> ")
        temp = temp.next
    print("None")
```
**Time Complexity:** O(n)

---
## **4. Real-Life Applications of Linked Lists**
| Application | Explanation |
|------------|------------|
| **Music Playlists** | Songs are linked to the next, allowing easy insertion/deletion. |
| **Undo/Redo Functionality** | Doubly Linked List enables moving forward and backward. |
| **Browser History** | Stores previous and next pages for easy navigation. |
| **Memory Management** | Used for dynamic memory allocation and garbage collection. |

---
## **5. Time Complexity of Linked List Operations**
| Operation | Singly Linked List | Doubly Linked List |
|-----------|-------------------|-------------------|
| **Insertion at Beginning** | O(1) | O(1) |
| **Insertion at End** | O(n) | O(1) |
| **Insertion at Position** | O(n) | O(n) |
| **Deletion at Beginning** | O(1) | O(1) |
| **Deletion at End** | O(n) | O(1) |
| **Deletion at Position** | O(n) | O(n) |
| **Traversal** | O(n) | O(n) |

---
## **6. Summary**
- **Linked lists** store elements dynamically.
- **Operations** include insertion, deletion, and traversal.
- **Types**: Singly, Doubly, Circular.
- **Used in** memory management, history tracking, and dynamic data structures.

Let me know if you need more details! 🚀




