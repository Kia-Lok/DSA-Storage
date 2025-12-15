# Dynamic Programming Problem Solving Methods
Repository containing Dynamic Programming Problems from Github and the various methods learnt to solve them

## Table of Contents
- [Kadane's Algorithm](#kadanes-algorithm)




## Kadane's Algorithm
Relevant Leetcode Problems: Maximum Subarray

Relevant applications: Finding maximum / minimum values in an array, especially if there are negative numbers in the array

Intuition: We want to determine if negative values are worth keeping in the maximum array. If we choose to exclude negative values, it means forgoing the positive values that are before the negative value. We approach this by keeping 2 values; 1 that stores the maximum possible value obtained and another that is an aggregate of the elements summed together. If the 2nd pointer ever goes negative, we reset it to equal the value of the next element since it shows its not worth including the past elements in the maximum array. 

Algorithm:
1. Initialise 2 integer variables and set them equal to the first element of the array
2. Iterate through the entire array starting from the second element. First, check if the subarray sum is negative. If it is, set it equal to the array element. If not, add the element to the subarray sum.
3. At each iteration, check the max value against the subarray sum. Max value equal subarray sum if subarray sum is larger
4. Return the max value



