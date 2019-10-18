## Sort

**Sort Algorithms**
1. Comparison sorts:
    - Bubble sort
    - Insertion sort
    - Selection sort
    - Merge sort
    - Quick sort

2. Linear sorts:
    - Bucket sort
    - Radix sort
    - Counting sort

**Problems**

- Largest number: return largest number by combining all strings, sort strings
by their combining value, then merge them.

- Merge interval: sort intervals by their start time, check if later interval
overlaps with last one and merge them.

- Valid triangle triplet: find triplet that can form triangle, sort array of number
for each number at i, find pair of j and k satisfy nums[j] + nums[k] > nums[i]
for j, k < i.

- Custom sort string: sort string T in order in string S. This problem is similar
counting sort, first count every char in T, and use order in S to append chars
to result.

- Sort colors: count color and put each color into result

- Maximum gap: find max difference between 2 successive numbers, can sort array and
compare every pair, run time is O(nlogn). If we want to improve run time, it
should use linear sort.
    - Use bucket sort with n+1 bucket, each bucket holds low and high value, max
    gap would be gap between low and high of 2 adjacent buckets.
