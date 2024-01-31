---
description: >-
  A linked list is a linear data structure where elements are stored in nodes,
  and each node points to the next node in the sequence.
---

# 😁 Linked List

{% hint style="info" %}
A drawback of linked lists is that access time is linear (and difficult to pipeline). Faster access, such as random access, is not feasible. Arrays have better cache locality as compared to linked lists.
{% endhint %}



<figure><img src="../../.gitbook/assets/linked-list.jpeg" alt=""><figcaption></figcaption></figure>

1.  **Node:**

    * Each node in a linked list contains two parts: data and a reference (or link) to the next node in the sequence.

    ```javascript
    class Node {
      constructor(data, next = null) {
        this.data = data;
        this.next = next;
      }
    }
    ```
2.  **Head:**

    * The head is the first node in the linked list. It serves as the starting point for traversal.

    ```javascript
    let head = new Node(1);
    ```
3.  **Traversal:**

    * To traverse a linked list, start from the head and follow the next pointers until the end (where the next pointer is null).

    ```javascript
    let current = head;
    while (current !== null) {
      console.log(current.data);
      current = current.next;
    }
    ```

#### Types of Linked Lists:

1. **Singly Linked List:**
   * Each node points to the next node in the sequence.
2. **Doubly Linked List:**
   * Each node points to both the next and the previous nodes in the sequence.
3. **Circular Linked List:**
   * In a circular linked list, the last node points back to the first node.

#### Operations on Linked Lists:

1.  **Insertion:**

    * Adding a new node to the linked list.

    ```javascript
    function insertAtEnd(head, data) {
      let newNode = new Node(data);
      if (head === null) {
        return newNode;
      }
      let current = head;
      while (current.next !== null) {
        current = current.next;
      }
      current.next = newNode;
      return head;
    }
    ```
2.  **Deletion:**

    * Removing a node from the linked list.

    ```javascript
    function deleteNode(head, targetData) {
      if (head === null) {
        return null;
      }
      if (head.data === targetData) {
        return head.next;
      }
      let current = head;
      while (current.next !== null && current.next.data !== targetData) {
        current = current.next;
      }
      if (current.next !== null) {
        current.next = current.next.next;
      }
      return head;
    }
    ```
3.  **Searching:**

    * Finding a node with a specific value.

    ```javascript
    function searchNode(head, targetData) {
      let current = head;
      while (current !== null) {
        if (current.data === targetData) {
          return true;
        }
        current = current.next;
      }
      return false;
    }
    ```
