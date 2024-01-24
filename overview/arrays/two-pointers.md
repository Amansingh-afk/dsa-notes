---
description: >-
  The Two Pointers technique is a strategy for efficiently solving problems by
  using two pointers that traverse an array or list.
---

# 😁 Two Pointers

{% hint style="info" %}
**Key Idea:** The two pointers can move towards each other, away from each other, or be at the same end, depending on the problem's requirements.
{% endhint %}

#### Basic Steps:

1. **Initialization:**
   * Set up two pointers at different positions in the array.
   * Usually, one pointer starts at the beginning, and the other starts at the end.
2. **Iterate Through the Array:**
   * Move the pointers based on the problem's logic.
   * Commonly used patterns include moving towards each other or away from each other.
3. **Do Something Useful:**
   * Perform required operations or checks on the elements pointed to by the two pointers.
4. **Adjust the Pointers:**
   * Move the pointers based on the problem's requirements.

#### Examples

{% code title="Two Sum Problem (Sorted Array):" %}
```javascript
function twoSumSorted(arr, target) {
  let left = 0;
  let right = arr.length - 1;

  while (left < right) {
    let sum = arr[left] + arr[right];

    if (sum === target) {
      return [arr[left], arr[right]];
    } else if (sum < target) {
      left++;
    } else {
      right--;
    }
  }

  return [];
}

let array = [2, 7, 11, 15];
let target = 9;
console.log(twoSumSorted(array, target)); // Output: [2, 7]
```
{% endcode %}
