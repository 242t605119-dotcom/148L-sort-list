# LeetCode 148 – Sort List

## Problem

Given the head of a singly linked list, sort the list in **ascending order**.

The solution should have:

* `O(n log n)` time complexity
* Constant extra space complexity if possible

## Example 1

**Input:**

```text
head = [4,2,1,3]
```

**Output:**

```text
[1,2,3,4]
```

## Example 2

**Input:**

```text
head = [-1,5,3,4,0]
```

**Output:**

```text
[-1,0,3,4,5]
```

## Example 3

**Input:**

```text
head = []
```

**Output:**

```text
[]
```

## Approach

The best approach for sorting a linked list efficiently is **Merge Sort**.

Merge Sort is well suited for linked lists because splitting and merging can be performed by changing node pointers rather than moving elements in an array.

The process has three main steps:

1. Find the middle of the linked list.
2. Split the list into two halves.
3. Recursively sort both halves and merge them.

### Example

For:

```text
4 → 2 → 1 → 3
```

Split into:

```text
4 → 2
1 → 3
```

Sort both parts:

```text
2 → 4
1 → 3
```

Merge them:

```text
1 → 2 → 3 → 4
```

## Algorithm

1. If the list has zero or one node, return it.
2. Use slow and fast pointers to find the middle.
3. Divide the list into two halves.
4. Recursively apply Merge Sort to both halves.
5. Merge the two sorted lists.
6. Return the merged sorted list.

## Why Merge Sort?

Common array sorting techniques such as Quick Sort can require additional handling when used with linked lists.

Merge Sort works naturally with linked lists because:

* Finding the middle can be done using two pointers.
* Nodes can be rearranged using pointers.
* Merging two sorted linked lists is efficient.
* The overall time complexity is `O(n log n)`.

## Complexity

* **Time Complexity:** `O(n log n)`
* **Space Complexity:** `O(log n)` for recursive calls.

The actual linked-list nodes do not require an additional array.

## LeetCode Details

* **Problem Number:** 148
* **Problem Name:** Sort List
* **Difficulty:** Medium
* **Language:** Python 3
* **File:** `solution.py`

## Topics

* Linked List
* Two Pointers
* Divide and Conquer
* Sorting
* Merge Sort

## Key Learning

This problem is a good example of applying **Divide and Conquer** to linked lists.

The key idea is to repeatedly divide the list into smaller parts, sort them, and then merge the sorted parts together.

## Repository Structure

```text
leetcode-148-sort-list/
│
├── solution.py
└── README.md
```

## Author

T.Nandhini
