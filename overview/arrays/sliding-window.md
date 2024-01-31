---
description: >-
  Sliding Window is a smart way to work with arrays or lists. It's like having a
  moving window that helps you process data efficiently.
---

# 😁 Sliding Window

{% hint style="info" %}
#### Key Idea: Instead of looking at each item one by one, the window lets you skip things that don't matter and focus only on what's important.
{% endhint %}

**Example: Finding Maximum Sum Subarray of Size `k`**

```javascript
function maxSumSubarray(arr, k) {
  let maxSum = 0;
  let currentSum = 0;

  // Get the sum of the first 'k' elements
  for (let i = 0; i < k; i++) {
    currentSum += arr[i];
  }

  // Go through the array
  for (let i = k; i < arr.length; i++) {
    // Update the sum by adding the new item and removing the first item of the window
    currentSum = currentSum + arr[i] - arr[i - k];
    // Check if this sum is the biggest so far
    maxSum = Math.max(maxSum, currentSum);
  }

  return maxSum;
}

let array = [1, 4, 2, 10, 2, 3, 1, 0, 20];
let k = 4;
console.log(maxSumSubarray(array, k)); // Output: 24
```

