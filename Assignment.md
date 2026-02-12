# ASSIGNMENT 1  
## TASK 1: Data Structure Classification and Applications  

**Programming Language Used:** Python  

---

# 1. Introduction  

Data structures are methods used to organize and store data efficiently so that it can be accessed and modified easily. Algorithms are step-by-step procedures used to solve problems by operating on these data structures.

Data structures are classified into:

- Primitive and Non-Primitive  
- Linear and Non-Linear  
- Static and Dynamic  

This assignment demonstrates these classifications using Python programming examples, explains their real-world applications, and discusses how data structures and algorithms function within computer systems.

---

# 2. Data Structure Classification  

## 2.1 Primitive Data Structures  

Primitive data structures store single values and are directly supported by programming languages.

### Types:
- Integer
- Float
- Character
- Boolean

### Code Example:

```python
# Primitive Data Structures

age = 21              # Integer
price = 19.99         # Float
grade = 'A'           # Character
is_registered = True  # Boolean

print(age, price, grade, is_registered)
```

### Applications:
- Storing user age, prices, grades, status values
- Used in all types of systems (banking, education, e-commerce)

### Reason:
They are simple, fast, memory-efficient, and form the foundation of more complex data structures.

---

## 2.2 Non-Primitive Data Structures  

Non-primitive data structures can store multiple values and are more complex.

They are divided into:

- Linear Data Structures  
- Non-Linear Data Structures  

---

# 3. Linear Data Structures  

Linear data structures store data in sequential order.

---

## 3.1 Array (Python List)

An array stores elements in contiguous memory locations and allows indexing.

### Code:

```python
# Array (List)

numbers = [10, 20, 30, 40, 50]

print("First element:", numbers[0])
```

### Applications:
- Storing student marks
- Product lists in shopping systems
- Employee records

### Example Systems:
- School Management Systems
- E-commerce platforms

### Reason:
Arrays allow fast access using index numbers (O(1) time complexity for access).

---

## 3.2 Linked List  

A linked list consists of nodes where each node points to the next node.

### Code:

```python
# Linked List Implementation

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

ll = LinkedList()
ll.append(1)
ll.append(2)
ll.append(3)
ll.display()
```

### Applications:
- Music playlists
- Browser navigation (Back and Forward buttons)

### Example Systems:
- Spotify playlist management
- Web browsers like Chrome

### Reason:
Efficient insertion and deletion without shifting elements.

---

## 3.3 Stack (LIFO – Last In First Out)

A stack follows the Last In First Out principle.

### Code:

```python
# Stack Implementation

stack = []

stack.append(10)
stack.append(20)
stack.append(30)

print("Removed:", stack.pop())
```

### Applications:
- Undo/Redo operations
- Function call management (Call Stack)

### Example Systems:
- Microsoft Word (Undo feature)
- Programming language compilers

### Reason:
The most recent operation is processed first.

---

## 3.4 Queue (FIFO – First In First Out)

A queue follows the First In First Out principle.

### Code:

```python
from collections import deque

queue = deque()

queue.append(10)
queue.append(20)
queue.append(30)

print("Removed:", queue.popleft())
```

### Applications:
- Printer queues
- CPU process scheduling

### Example Systems:
- Banking systems
- Operating systems

### Reason:
Ensures fair processing order.

---

# 4. Non-Linear Data Structures  

Non-linear data structures store data hierarchically or in interconnected form.

---

## 4.1 Tree  

A tree represents hierarchical relationships.

### Code:

```python
# Simple Binary Tree

class TreeNode:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None

root = TreeNode(10)
root.left = TreeNode(5)
root.right = TreeNode(15)

print("Root:", root.value)
```

### Applications:
- File systems
- Database indexing (Binary Search Trees, B-Trees)
- HTML DOM structure

### Example Systems:
- Windows File Explorer
- MySQL Database

### Reason:
Allows efficient searching, insertion, and deletion in hierarchical data.

---

## 4.2 Graph  

A graph represents relationships between entities.

### Code:

```python
# Graph using adjacency list

graph = {
    "A": ["B", "C"],
    "B": ["A", "D"],
    "C": ["A"],
    "D": ["B"]
}

print("Connections of A:", graph["A"])
```

### Applications:
- Social networks
- GPS navigation systems
- Network routing

### Example Systems:
- Facebook (friend connections)
- Google Maps

### Reason:
Graphs model real-world relationships effectively.

---

# 5. Static vs Dynamic Data Structures  

## Static Data Structures
- Fixed size
- Memory allocated at compile time
- Example: Array

## Dynamic Data Structures
- Size can change during runtime
- Memory allocated dynamically
- Examples: Linked List, Stack, Queue, Trees, Graphs

### Reason:
Dynamic structures are more flexible and efficient for growing data.

---

# 6. How Data Structures and Algorithms Work Within Systems  

Data structures store and organize data in memory.  
Algorithms perform operations such as searching, sorting, inserting, and deleting.

## Real System Examples:

### 1. Google Maps
- Graph stores roads and locations.
- Dijkstra’s Algorithm finds shortest path.

### 2. Search Engines
- Trees and hash tables index web pages.
- Search algorithms retrieve results quickly.

### 3. Operating Systems
- Queues manage running processes.
- Scheduling algorithms control execution order.

### 4. Databases
- B-Trees store indexed records.
- Sorting and searching algorithms improve performance.

---

# 7. Importance of Choosing the Correct Data Structure  

Choosing the right data structure:

- Improves speed and performance
- Reduces memory usage
- Increases scalability
- Enhances system efficiency

Example:  
Using a linked list instead of an array for frequent insertions improves performance because elements do not need to be shifted.
