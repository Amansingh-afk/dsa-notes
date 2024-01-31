# 💀 DP

#### 1. **Optimization Problems:**

**Example - Fibonacci Sequence:**

* **Problem:**
  * Find the nth Fibonacci number.
*   **Recursive Approach (Without DP):**

    ```javascript
    function fibonacci(n) {
      if (n <= 1) {
        return n;
      } else {
        return fibonacci(n - 1) + fibonacci(n - 2);
      }
    }
    ```
* **Issues:**
  * This recursive approach leads to exponential time complexity due to redundant calculations.
*   **DP Approach with Memoization:**

    ```javascript
    function fibonacciDP(n, memo = {}) {
      if (n <= 1) {
        return n;
      } else if (memo[n] !== undefined) {
        return memo[n];
      } else {
        memo[n] = fibonacciDP(n - 1, memo) + fibonacciDP(n - 2, memo);
        return memo[n];
      }
    }
    ```
* **Benefits:**
  * Memoization ensures that each Fibonacci number is calculated only once, significantly improving efficiency.

#### 2. **Sequence Problems:**

**Example - Longest Increasing Subsequence:**

* **Problem:**
  * Given an array, find the length of the longest increasing subsequence.
*   **DP Approach (Bottom-Up):**

    ```javascript
    function longestIncreasingSubsequence(nums) {
      const n = nums.length;
      const dp = new Array(n).fill(1);

      for (let i = 1; i < n; i++) {
        for (let j = 0; j < i; j++) {
          if (nums[i] > nums[j] && dp[i] < dp[j] + 1) {
            dp[i] = dp[j] + 1;
          }
        }
      }

      return Math.max(...dp);
    }
    ```
* **Explanation:**
  * The DP array (`dp`) keeps track of the length of the longest increasing subsequence ending at each position.
  * The nested loop compares elements to find increasing subsequences and updates the DP array accordingly.

#### 3. **Graph Algorithms:**

**Example - Shortest Path in a Weighted Graph:**

* **Problem:**
  * Find the shortest path from a source node to all other nodes in a weighted graph.
*   **DP Approach (Dijkstra's Algorithm):**

    ```javascript
    function dijkstra(graph, source) {
      const n = graph.length;
      const dist = new Array(n).fill(Infinity);
      dist[source] = 0;

      const visited = new Set();

      while (visited.size < n) {
        const u = getMinDistanceNode(dist, visited);
        visited.add(u);

        for (let v = 0; v < n; v++) {
          if (!visited.has(v) && graph[u][v] !== 0 && dist[u] !== Infinity && dist[u] + graph[u][v] < dist[v]) {
            dist[v] = dist[u] + graph[u][v];
          }
        }
      }

      return dist;
    }
    ```
* **Explanation:**
  * `dist` array keeps track of the shortest distances from the source node.
  * The algorithm iteratively selects the node with the minimum distance, updates its neighbors' distances, and marks it as visited.

\
