# Maximum-Frequency-After-Subarray-Operation

Problem Description :

You are given an array nums of length n and an integer k.
You perform the following operation on nums once:
Select a subarray nums[i..j] where 0 <= i <= j <= n - 1.
Select an integer x and add x to all the elements in nums[i..j].
Find the maximum frequency of the value k in the array after performing the operation.

Algorithm : 

Count Initial Occurrences: Use a frequency array to count the occurrences of each value in nums.
Identify Maximum Frequency of k:
To make any element in a subarray equal to k, calculate the value of x needed as x = k - nums[m] for each index m.
Keep track of the range of indices where this transformation can occur using prefix sums.
Track Overlapping Subarrays: Use a sliding window technique to track the number of indices where the value becomes k after adding x.
Return Maximum Frequency: Compute the maximum count of k achievable after a single operation.

Key Observations : 

The problem can be solved efficiently by leveraging prefix sums and frequency maps.
Only values in the range [1, 50] need to be considered due to constraints, reducing complexity.

Complexity :

Time Complexity: O(n) as we iterate through the array once.
Space Complexity: O(1) (ignoring input and output size) since we only use fixed-size arrays for tracking frequencies.
