---
description: >-
  Kadane's Algorithm is a simple and efficient approach for finding the maximum
  sum subarray within a given array.
---

# 😁 Kadane's

{% hint style="info" %}
**Key Idea**: It focuses on keeping track of the maximum sum ending at each position in the array and overall maximum sum.
{% endhint %}

#### Basic Steps:

1. **Initialize Variables:**
   * `maxEndingHere`: Maximum sum ending at the current position.
   * `maxSoFar`: Overall maximum sum.
2. **Iterate Through the Array:**
   * For each element, update `maxEndingHere` by taking the maximum of the current element and the sum of `maxEndingHere` and the current element.
   * Update `maxSoFar` by taking the maximum of `maxSoFar` and `maxEndingHere`.

#### Examples

{% code title="Kadane's Algorithm " %}
```javascript
function kadanesAlgorithm(arr) {
  let maxEndingHere = arr[0];
  let maxSoFar = arr[0];

  for (let i = 1; i < arr.length; i++) {
    maxEndingHere = Math.max(arr[i], maxEndingHere + arr[i]);
    maxSoFar = Math.max(maxSoFar, maxEndingHere);
  }

  return maxSoFar;
}

let array = [-2, 1, -3, 4, -1, 2, 1, -5, 4];
console.log(kadanesAlgorithm(array)); // Output: 6
```
{% endcode %}
