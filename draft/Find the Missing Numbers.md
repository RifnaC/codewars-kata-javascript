## Questions
You are given an unsorted array of unique integers in the range of 1 to n. However, k numbers are missing from the array.

Your task is to write a function findMissingNumbers(arr, n, k) that takes three parameters:

arr is the unsorted array of integers
n is the highest integer in the range
k is the number of missing integers
The function should return an array of the missing integers in ascending order.

The array arr will have a length of n - k, 1 <= n, k <= 10^5.

## Example
```javascript
findMissingNumbers([5, 2, 1, 7], 8, 3); // Output: [3, 4, 6]
findMissingNumbers([10, 3, 6, 7, 4, 8], 10, 4); // Output: [1, 2, 5, 9]
```

## Constraints
The input array arr will contain integers in the range of 1 to n with no duplicates.
The number of missing integers k is guaranteed to be accurate.
The time complexity of your solution should not exceed O(n).
The space complexity of your solution should not exceed O(n).

## Bonus challenge(s) *for fun
Modify the findMissingNumbers function to accept an optional boolean parameter 'includeNegatives'. When this parameter is set to true, the function should also consider the negative integers from -n to -1 in the range. In this case, the input array arr will have a length of 2n - k, -10^5 <= n, k <= 10^5. The function should return an array of missing integers in ascending order, including the missing negative integers if any.

example / test case

```javascript
findMissingNumbers([-4, -1, 0, 1, 4], 5, 4, true); // Output: [-5, -3, -2, 2, 3]
findMissingNumbers([5, -7, -5, 0, 2, 4], 7, 5, true); // Output: [-6, -4, -3, 1, 3]
```

Write a function called 'encodeMessage' that takes an array of missing integers (returned by findMissingNumbers) and encodes them into a string of lowercase English letters (a-z) using a substitution cipher with a given shift value. The shift value is constant for all letters in the message. The function should have the following signature: encodeMessage(missingNumbers, shift)

example / test case

```javascript
encodeMessage([-5, -3, -2, 2, 3], 3); // Output: 'aefgh'
encodeMessage([1, 4, 7, 10, 11], 5); // Output: 'fmjqv'
```
Note: You can assume that the length of the missing numbers array will not exceed 26, so there will be no need to wrap around the alphabet.


