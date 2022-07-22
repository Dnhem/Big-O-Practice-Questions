### Step One: Simplifying Expressions
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

<code>
function logUpTo(n) {
  for (let i = 1; i <= n; i++) {
    console.log(i);
  }
}
</code>
Time Complexity: O(n)\
<code>
function logAtLeast10(n) {
  for (let i = 1; i <= Math.max(n, 10); i++) {
    console.log(i);
  }
}
</code>
Time Complexity:\
<code>
function logAtMost10(n) {
  for (let i = 1; i <= Math.min(n, 10); i++) {
    console.log(i);
  }
}
</code>
Time Complexity:\
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
Time Complexity:\

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
Time Complexity:\

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
Time Complexity:\