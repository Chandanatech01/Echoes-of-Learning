# 💾 Space Complexity and Data Structure Classification

This document provides a simple overview of **Space Complexity** and introduces the primary classifications of **Data Structures (DS)**: Linear, Non-Linear, and Hash-Based.

---

## 1. Space Complexity (Simple View)

**Space Complexity** is the measure of how much **memory (RAM)** an algorithm needs to run and finish its job.

We use **Big O notation** ($O$) to describe this. It doesn't tell us the exact number of bytes, but rather **how the memory usage grows** as the size of the input data ($n$) increases.

### Key Memory Components

1.  **Fixed Space:** The memory used for the program code and simple variables (like `int x`). This memory **stays the same** regardless of the input size $n$.
2.  **Variable Space (Auxiliary Space):** The memory used for data structures (like arrays, lists, or recursion stacks) that **grow or shrink** based on the input size $n$. This is the part we analyze with Big O.

### Common Space Complexities

| Big O Notation | Meaning | Simple Analogy | Example Data Structure |
| :--- | :--- | :--- | :--- |
| **$O(1)$** | **Constant Space** | The memory needed is fixed. It doesn't matter if the input is 1 item or 1 million items. | Storing a few fixed-size variables (e.g., $a, b, c$). |
| **$O(n)$** | **Linear Space** | The memory needed grows **directly** with the size of the input $n$. | Storing all $n$ items in a single-dimensional **Array** or **Linked List**. |
| **$O(n^2)$** | **Quadratic Space** | The memory needed grows by the **square** of the input size $n$. | Storing an $n \times n$ grid or a two-dimensional array. |

---

## 2. Classification of Data Structures

Data structures are categorized based on how their data elements are **arranged** and **connected**.

### A. Linear Data Structures

Elements are arranged in a **sequential** or **straight-line** fashion. Each element is linked to at most one predecessor and one successor.

| DS Type | Brief Introduction | Key Characteristics |
| :--- | :--- | :--- |
| **Arrays** | A collection of elements stored at **adjacent memory locations**. Accessing an element by its index is extremely fast. | Fixed size (in many languages); **$O(1)$** time for random access. |
| **Linked Lists** | A sequence of **nodes**, where each node contains the data and a **pointer** to the next node. | Dynamic size; sequential access; efficient insertions and deletions. |
| **Stacks** | Follows the **LIFO** (Last-In, First-Out) principle. Elements are only added (**Push**) and removed (**Pop**) from the **top**. | Used for managing function calls and browser history (back button). |
| **Queues** | Follows the **FIFO** (First-In, First-Out) principle. Elements are added at the **rear** and removed from the **front**. | Used in task scheduling and waiting lines (like a print queue). |

---

### B. Non-Linear Data Structures

Elements are **not sequential**. They can be connected to multiple other elements, forming complex relationships or hierarchies.

| DS Type | Brief Introduction | Key Characteristics |
| :--- | :--- | :--- |
| **Trees** | A hierarchical structure starting with a single node (the **root**). Every node has at most one parent but can have multiple children. | Used for representing file systems, organizational charts, and search indexes (e.g., Binary Search Tree). |
| **Graphs** | A collection of **vertices (nodes)** and **edges** (the connections between them). Used to model networks. | Highly flexible; models relationships like social networks or city road maps. |
| **Heaps** | A specialized tree (usually binary) that maintains the **heap property**: the largest/smallest item is always at the root. | Used to efficiently implement **Priority Queues** and the Heap Sort algorithm. |

---

### C. Hash-Based Data Structures

These structures rely on a **hash function** to quickly map a **key** to a storage location (index) in memory. This provides extremely fast lookups.

| DS Type | Brief Introduction | Key Characteristics |
| :--- | :--- | :--- |
| **Hash Tables / Hash Maps** | Stores data as **key-value pairs**. The hash function calculates the address where the value is stored using its key. | Offers average **$O(1)$** time for insertion, deletion, and search (very fast). |
| **Sets (HashSets)** | A collection used to store **unique, unordered** elements. Duplicates are not allowed. | Optimized for quick membership testing (checking if an element exists). |
