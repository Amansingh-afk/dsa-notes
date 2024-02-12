---
description: >-
  JavaScript array methods. A categorized list of these methods, along with
  short descriptions and examples for each. ~Be ready to implement this
  features/methods in other languages~
---

# 🔥 Array methods.

### Adding

<table><thead><tr><th width="152">Command</th><th>Description</th><th>Example</th></tr></thead><tbody><tr><td><code>.push()</code></td><td>Add anything to the end of an array.</td><td><code>let a = []; let b = {}; a.push(b); console.log(a[0] === b); // true</code></td></tr><tr><td><code>.push()</code></td><td>Add more than one item at a time.</td><td><code>let x = ['a']; x.push('b', 'c'); console.log(x); // ['a', 'b', 'c']</code></td></tr><tr><td><code>.unshift()</code></td><td>Add to the beginning of an array and returns the new length.</td><td><code>let x = ['c', 'd']; x.unshift('a', 'b'); console.log(x); // ['a', 'b', 'c', 'd']</code></td></tr><tr><td><code>.splice()</code></td><td>Add an element to an arbitrary location.</td><td><code>let a = [1, 2, 3, 4]; a.splice(2, 0, 'foo'); console.log(a); // [1, 2, "foo", 3, 4]</code></td></tr></tbody></table>

### Reorganizing

<table><thead><tr><th width="185">Command</th><th>Description</th><th>Example</th></tr></thead><tbody><tr><td><code>.copyWithin()</code></td><td>Copy part of an array to another location within the same array.</td><td><code>let a = ['a', 'b', 'c', 'd', 'e']; a.copyWithin(0, 3, 4); console.log(a); // ["d", "b", "c", "d", "e"]</code></td></tr><tr><td><code>.slice()</code></td><td>Returns a portion of an array selected from start to end.</td><td><code>let a = ['ant', 'bison', 'camel', 'duck', 'elephant']; console.log(a.slice(2)); // ["camel", "duck", "elephant"]</code></td></tr><tr><td><code>.splice()</code></td><td>Replace an arbitrary element in the array.</td><td><code>let a = [1, 2, 3, 4]; a.splice(2, 1, 'foo'); console.log(a); // [1, 2, "foo", 4]</code></td></tr></tbody></table>

### Combining

<table><thead><tr><th width="150">Command</th><th>Description</th><th>Example</th></tr></thead><tbody><tr><td><code>.concat()</code></td><td>Create a new array from two arrays.</td><td><code>let x = ['a', 'b', 'c']; let y = ['d', 'e', 'f']; let z = x.concat(y); console.log(z); // ['a', 'b', 'c', 'd', 'e', 'f']</code></td></tr><tr><td><code>...</code></td><td>Not a method, but create a new array from two arrays by spreading them.</td><td><code>let x = ['a', 'b']; let y = ['c', 'd']; let z = [...x, ...y]; console.log(z); // ['a', 'b', 'c', 'd']</code></td></tr></tbody></table>

### Removing

<table><thead><tr><th width="146">Command</th><th>Description</th><th>Example</th></tr></thead><tbody><tr><td><code>.pop()</code></td><td>Removes the last element from an array and returns it.</td><td><code>let a = ['a', 'b', 'c']; a.pop(); console.log(a); // ["a", "b"]</code></td></tr><tr><td><code>.shift()</code></td><td>Removes the first element from an array and returns it.</td><td><code>let a = ['a', 'b', 'c']; a.shift(); console.log(a); // ["b", "c"]</code></td></tr><tr><td><code>.splice()</code></td><td>Remove elements from an arbitrary location.</td><td><code>let a = ['a', 'b', 'c', 'd', 'e']; a.splice(1, 3); console.log(a); // ["a", "e"]</code></td></tr></tbody></table>

### Filtering/Searching

<table><thead><tr><th width="191">Command</th><th>Description</th><th>Example</th></tr></thead><tbody><tr><td><code>.filter()</code></td><td>Keeps the items in the array that pass the test provided by the callback function.</td><td><code>let a = ['foo', 'bar', 'fooz']; let b = a.filter(v => v.startsWith('foo')); console.log(b); // ['foo', 'fooz']</code></td></tr><tr><td><code>.find()</code></td><td>Finds the first item in an array that matches.</td><td><code>let a = [5, 12, 8, 130, 44]; let b = a.find(v => v > 10); console.log(b); // 12</code></td></tr><tr><td><code>.findIndex()</code></td><td>Like find but returns the index.</td><td><code>let a = [5, 12, 8, 130, 44]; let b = a.findIndex(v => v > 13); console.log(b); // 3</code></td></tr><tr><td><code>.indexOf()</code></td><td>Finds the first index of an element.</td><td><code>let a = ['foo', 'bar', 'baz']; console.log(a.indexOf('baz')); // 2</code></td></tr><tr><td><code>.lastIndexOf()</code></td><td>Like indexOf, but finds the last index.</td><td><code>let a = ['foo', 'bar', 'baz', 'foo']; console.log(a.lastIndexOf('foo')); // 3</code></td></tr></tbody></table>

### Sorting

<table><thead><tr><th width="130">Command</th><th>Description</th><th>Example</th></tr></thead><tbody><tr><td><code>.sort()</code></td><td>Sort alphabetically.</td><td><code>let a = ['d', 'j', 'a', 'b', 'c', 'g']; a.sort(); console.log(a); // ["a", "b", "c", "d", "g", "j"]</code></td></tr><tr><td><code>.sort()</code></td><td>Sort in reversed alphabetical order.</td><td><code>let a = ['d', 'j', 'a', 'b', 'c', 'g']; a.sort().reverse(); console.log(a); // ["j", "g", "d", "c", "b", "a"]</code></td></tr><tr><td><code>.sort()</code></td><td>Sort numerically.</td><td><code>let a = [5, 10, 7, 1, 3, 2]; a.sort((a, b) => a - b); console.log(a); // [1, 2, 3, 5, 7, 10]</code></td></tr><tr><td><code>.sort()</code></td><td>Descending numerical sort.</td><td><code>let a = [5, 10, 7, 1, 3, 2]; a.sort((a, b) => b - a); console.log(a); // [10, 7, 5, 3, 2, 1]</code></td></tr></tbody></table>

### Loop Structures

<table><thead><tr><th width="153">Command</th><th>Description</th><th>Example</th></tr></thead><tbody><tr><td><code>.map()</code></td><td>Maps each element to a new element by applying a function.</td><td><code>let a = [1, 2, 3, 4]; let b = a.map(v => v * 2); console.log(b); // [2, 4, 6, 8]</code></td></tr><tr><td><code>.flatMap()</code></td><td>Maps each element to a new array and flattens it.</td><td><code>let a = [1, 2, 3, 4]; let b = a.flatMap(v => [v * 2]); console.log(b); // [2, 4, 6, 8]</code></td></tr><tr><td><code>.forEach()</code></td><td>Executes a function for each array element.</td><td><code>let a = [1, 2]; a.forEach(x => console.log(x)); // 1 2</code></td></tr></tbody></table>

### Booleans

<table><thead><tr><th width="167">Command</th><th>Description</th><th>Example</th></tr></thead><tbody><tr><td><code>.every()</code></td><td>Tests if every element passes the test.</td><td><code>let isBelowThreshold = (currentValue) => currentValue &#x3C; 40; let array = [1, 30, 39, 29, 10, 13]; console.log(array.every(isBelowThreshold)); // true</code></td></tr><tr><td><code>.some()</code></td><td>Tests if any of the elements pass the test.</td><td><code>let exists = (element) => element > 20; let array = [1, 30, 39, 29, 10, 13]; console.log(array.some(exists)); // true</code></td></tr><tr><td><code>.includes()</code></td><td>Checks if an array includes a certain value.</td><td><code>let array = [1, 2, 3]; console.log(array.includes(2)); // true</code></td></tr></tbody></table>

### Creating

<table><thead><tr><th width="181">Command</th><th>Description</th><th>Example</th></tr></thead><tbody><tr><td><code>Array.of()</code></td><td>Creates a new Array instance from a variable number of arguments.</td><td><code>console.log(Array.of(7)); // [7]</code></td></tr><tr><td><code>Array.from()</code></td><td>Creates a new, shallow-copied Array instance from an array-like or iterable object.</td><td><code>console.log(Array.from('foo')); // ['f', 'o', 'o']</code></td></tr><tr><td><code>.fill()</code></td><td>Fills all the elements of an array from a start index to an end index with a static value.</td><td><code>let array = [1, 2, 3, 4]; console.log(array.fill(0, 2, 4)); // [1, 2, 0, 0]</code></td></tr></tbody></table>

### Morphing

<table><thead><tr><th width="221">Command</th><th>Description</th><th>Example</th></tr></thead><tbody><tr><td><code>.entries()</code></td><td>Returns a new Array Iterator object that contains the key/value pairs for each index in the array.</td><td><code>let array = ['a', 'b', 'c']; let iterator = array.entries(); console.log(iterator.next().value); // [0, 'a']</code></td></tr><tr><td><code>.values()</code></td><td>Returns a new Array Iterator object that contains the values for each index in the array.</td><td><code>let array = ['a', 'b', 'c']; let iterator = array.values(); for (const value of iterator) { console.log(value); } // 'a' 'b' 'c'</code></td></tr><tr><td><code>.keys()</code></td><td>Returns a new Array Iterator that contains the keys for each index in the array.</td><td><code>let array = ['a', 'b', 'c']; let iterator = array.keys(); for (const key of iterator) { console.log(key); } // 0 1 2</code></td></tr><tr><td><code>.join()</code></td><td>Joins all elements of an array into a string.</td><td><code>let array = ['Fire', 'Air', 'Water']; console.log(array.join()); // "Fire,Air,Water"</code></td></tr><tr><td><code>.toString()</code></td><td>Returns a string representing the specified array and its elements.</td><td><code>let array = ['Jan', 'Feb', 'Mar', 'Apr']; console.log(array.toString()); // "Jan,Feb,Mar,Apr"</code></td></tr><tr><td><code>.toLocaleString()</code></td><td>Returns a localized string representing the array and its elements.</td><td><code>let array = [1, 'a', new Date('21 Dec 1997 14:12:00 UTC')]; console.log(array.toLocaleString('en', { timeZone: 'UTC' })); // "1,a,12/21/1997, 2:12:00 PM"</code></td></tr></tbody></table>

### Information

<table><thead><tr><th width="203">Command</th><th>Description</th><th>Example</th></tr></thead><tbody><tr><td><code>.at()</code></td><td>Returns the array item at the given index. Accepts negative integers to count from the end.</td><td><code>let array = ['a', 'b', 'c']; console.log(array.at(-1)); // 'c'</code></td></tr><tr><td><code>.length</code></td><td>Property that returns or sets the number of elements in an array.</td><td><code>let array = ['a', 'b', 'c']; console.log(array.length); // 3</code></td></tr><tr><td><code>Array.isArray()</code></td><td>Returns true if the argument is an array, or false otherwise.</td><td><code>let array = [1, 2, 3]; console.log(Array.isArray(array)); // true</code></td></tr></tbody></table>

### Misc.

<table><thead><tr><th width="152">Command</th><th>Description</th><th>Example</th></tr></thead><tbody><tr><td><code>.flat()</code></td><td>Creates a new array with all sub-array elements concatenated into it recursively up to the specified depth.</td><td><code>let array = [0, 1, 2, [3, 4]]; console.log(array.flat()); // [0, 1, 2, 3, 4]</code></td></tr><tr><td><code>.reverse()</code></td><td>Reverses an array in place. The first array element becomes the last, and the last array element becomes the first.</td><td><code>let array = [1, 2, 3, 4]; array.reverse(); console.log(array); // [4, 3, 2, 1]</code></td></tr></tbody></table>
