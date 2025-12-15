# Dynamic Programming Problem Solving Methods
Repository containing Dynamic Programming Problems from Github and the various methods learnt to solve them

## Table of Contents
- [Kadane's Algorithm](#kadanes-algorithm)
- [Top Down](#top-down)
- [Bottom Up](#bottom-up)




## Kadane's Algorithm
Relevant Leetcode Problems: Maximum Subarray

Relevant applications: Finding maximum / minimum values in an array, especially if there are negative numbers in the array

Intuition: We want to determine if negative values are worth keeping in the maximum array. If we choose to exclude negative values, it means forgoing the positive values that are before the negative value. We approach this by keeping 2 values; 1 that stores the maximum possible value obtained and another that is an aggregate of the elements summed together. If the 2nd pointer ever goes negative, we reset it to equal the value of the next element since it shows its not worth including the past elements in the maximum array. 

Algorithm:
1. Initialise 2 integer variables and set them equal to the first element of the array
2. Iterate through the entire array starting from the second element. First, check if the subarray sum is negative. If it is, set it equal to the array element. If not, add the element to the subarray sum.
3. At each iteration, check the max value against the subarray sum. Max value equal subarray sum if subarray sum is larger
4. Return the max value

## Top Down
Relevant Leetcode Problems: Jump Game

Relevant Applications: Backtracking but with time-complexity matters

Intuition: Backtracking is a common recursive solution to DP problems. However, tree recursion can give rise to O(2^n) time complexity, making it very inefficient. The next step to approach DP problem after naive backtracking is to implement memoization. It relies on the fact that once an index is deemed to give a good/bad result, it will stay like that, allowing for the result to be used immediately rather than computing again. Hence, memoization table is used to store such results.

Algorithm:
1) Initialize a memoization table (array) and assign UNKNOWN (or equivalent) to each position of the array except for the end index which is trivially GOOD.
2) Perform backtracking recursion. This time first check the memo table if the result had been computed before. If so, use the result and return. Else, compute and store the result in the memo table

## Bottom Up
Relevant Leetcode Problems: Jump Game

Relevant Applications: Converting top down to bottom up if recursion is not allowed / stricter time and space complexity


