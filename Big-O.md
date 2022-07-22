### Simplifying Expressions
#### Simplify the following big O expressions as much as possible:

O(n + 10) --> **O(n)** *Linear*\
O(100 * n) --> **O(n)** *Linear*\
O(25) --> **O(1)** *Constant* \
O(n^2 + n^3) --> **O(n^3)** *Cubic*\
O(n + n + n + n) --> **O(n)** *Linear*\
O(1000 * log(n) + n) --> **O(n)** *Linear*\
O(1000 * n * log(n) + n) --> **O(n log n)** *Logarithmic*\
O(2^n + n^2) --> **O(2^n)** *Exponential*\
O(5 + 3 + 1) --> **O(1)** *Constant*\
O(n + n^(1/2) + n^2 + n * log(n)^10) --> **O(n^2)** *Quadratic*

### Calculating Time Complexity

<code>
function logUpTo(n) {
  for (let i = 1; i <= n; i++) {
    console.log(i);
  }
}
</code>
Time Complexity: O(n)
<br>
<br>
<code>
function logAtLeast10(n) {
  for (let i = 1; i <= Math.max(n, 10); i++) {
    console.log(i);
  }
}
</code>
Time Complexity: O(n)
<br>
<br>
<code>
function logAtMost10(n) {
  for (let i = 1; i <= Math.min(n, 10); i++) {
    console.log(i);
  }
}
</code>
Time Complexity: O(1)
<br>
<br>
<code>
function onlyElementsAtEvenIndex(array) {
  let newArray = [];
  for (let i = 0; i < array.length; i++) {
    if (i % 2 === 0) {
      newArray.push(array[i]);
    }
  }
  return newArray;
}
</code>
Time Complexity: O(n)
<br>
<br>
<code>
function subtotals(array) {
  let subtotalArray = [];
  for (let i = 0; i < array.length; i++) {
    let subtotal = 0;
    for (let j = 0; j <= i; j++) {
      subtotal += array[j];
    }
    subtotalArray.push(subtotal);
  }
  return subtotalArray;
}
</code>
Time Complexity: O(n^2)
<br>
<br>
<code>
function vowelCount(str) {
  let vowelCount = {};
  const vowels = "aeiouAEIOU";
  for (let char of str) {
    if(vowels.includes(char)) {
      if(char in vowelCount) {
        vowelCount[char] += 1;
      } else {
        vowelCount[char] = 1;
      }
    }
  }

  return vowelCount;
}
</code>
Time Complexity: O(n)
<br>

### short answer

True or false: n^2 + n is O(n^2). \
True or false: n^2 * n is O(n^3). \
True or false: n^2 + n is O(n). \
What’s the time complexity of the .indexOf array method? \
What’s the time complexity of the .includes array method? \
What’s the time complexity of the .forEach array method? \
What’s the time complexity of the .sort array method? \
What’s the time complexity of the .unshift array method? \
What’s the time complexity of the .push array method? \
What’s the time complexity of the .splice array method? \
What’s the time complexity of the .pop array method? \
What’s the time complexity of the Object.keys() function? 