---
description: >-
  Bit manipulation involves the manipulation of individual bits in a binary
  representation of data.
---

# 💱 Bit Manipulation

Common Bitwise Operators:

1.  **AND (&):**

    * Sets each bit to 1 if both bits are 1.

    ```javascript
    let result = 5 & 3; // Binary: 0101 & 0011 = 0001 (Decimal: 1)
    ```
2.  **OR (|):**

    * Sets each bit to 1 if at least one of the corresponding bits is 1.

    ```javascript
    let result = 5 | 3; // Binary: 0101 | 0011 = 0111 (Decimal: 7)
    ```
3.  **XOR (^):**

    * Sets each bit to 1 if only one of the corresponding bits is 1.

    ```javascript
    let result = 5 ^ 3; // Binary: 0101 ^ 0011 = 0110 (Decimal: 6)
    ```
4.  **NOT (\~):**

    * Flips the bits, changing 0s to 1s and 1s to 0s.

    ```javascript
    let result = ~5; // Binary: ~0101 = 1010 (Decimal: -6)
    ```
5.  **Left Shift (<<):**

    * Shifts the bits to the left by a specified number of positions.

    ```javascript
    let result = 5 << 1; // Binary: 0101 << 1 = 1010 (Decimal: 10)
    ```
6.  **Right Shift (>>):**

    * Shifts the bits to the right by a specified number of positions.

    ```javascript
    let result = 5 >> 1; // Binary: 0101 >> 1 = 0010 (Decimal: 2)
    ```

#### Use Cases:

1.  **Bitwise AND to Check Odd or Even:**

    * Checking the last bit to determine whether a number is odd or even.

    ```javascript
    let isEven = (num & 1) === 0;
    ```
2.  **Bitwise XOR Swap:**

    * Swapping values without using a temporary variable.

    ```javascript
    let a = 5, b = 3;
    a = a ^ b;
    b = a ^ b;
    a = a ^ b;
    ```
3.  **Setting/Unsetting a Bit:**

    * Setting a specific bit to 1 or 0.

    ```javascript
    // Set the 3rd bit to 1
    let value = 5 | (1 << 2);

    // Unset the 2nd bit to 0
    value = 7 & ~(1 << 1);
    ```

