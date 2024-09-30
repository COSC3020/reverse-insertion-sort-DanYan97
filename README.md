# Reverse Insertion Sort

Consider the code for insertion sort we covered in class:

```javascript
function insertionSortReverse(arr) {
  for(var i = arr.length-2; i >= 0; i--) {
    var val = arr[i];
    var j;
    for(j = i; j < arr.length-1 && arr[j+1] < val; j++) {
      arr[j] = arr[j+1];
    }
    arr[j] = val;
  }
  return arr;
}
```

Change this function such that it works from the end of the array rather than
the beginning, `insertionSortReverse()` -- only the direction of
iterating over the elements is reversed, the array is still sorted the same way
(ascending). Add your code in `code.js`. Test your new function; I've provided
some basic testing code that uses [jsverify](https://jsverify.github.io/) in
`code.test.js`.

## Average-Case Time Complexity of Insertion Sort

In the lectures, we covered that insertion sort has best-case time complexity of
$\Theta(n)$ and worst-case time complexity of $\Theta(n^2)$. What is the
average-case time complexity ($\Theta$)?

Hint: Think about what happens in each iteration of the loop, and how often the
loop is executed. Keep in mind that for asymptotic analysis we don't care about
constant factors.

Describe your reasoning and the conclusion you've come to. Your reasoning is
most important -- you can easily find the answer, but you need to demonstrate
that you've understood the concept. Add your answer to this markdown file.

The inner loop for each element, on average, it would be about i/2 times, becuase 
about half of the elements before the current are larger and needs to be shifted. 
Whereas the outer loop runs n times, once for each.Therefore, the time complexity
can be represented as n^2/2. The constant 1/2 can be ignored, so the average case 
 time complexity would be ($\Theta(n^2)$)

 “I certify that I have listed all sources used to complete this exercise, including 
 the use of any Large Language Models. All of the work is my own, except where stated 
 otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism 
 is suspected, charges may be filed against me without prior notice.” --Doris Yan
