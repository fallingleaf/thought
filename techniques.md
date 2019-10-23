## Techniques
- This provides some helpful tips or techniques to help solve algorithm
problems, or simply improve runtime of algorithms.


**Pre-process Data**
- When input data is repeatedly used to calculate against other input data.
- Questions:
  1. Find longest word in dictionary that subsequence of given string S:
    - one simple approach is comparing S with each of word in dictionary and
    return the longest word.
    - S is used multiple times, it could be preprocessed, use a dict to store
    all index for each char in S. When compare word, check each char from word,
    and use binary search to find for first char index in S that equal or larger
    then previous index.
    - Word list can also be pre-processed, we can group all words by their current
    char need to compare with S, store word by (word, index) where index is current
    char index, and use a dict to group these words. e.g 'a' -> [('apple', 0), ('ale', 0)]
    scan each char in S, look for word group in dict and increase their index as
    well as next char.
  2. Trapping rain water:
    - This problem can be solved by finding max from left side and right side,
    deduct to current height at each column.
    - Finding max left and right for each column is redundant, we can pre-process
    and store max left and right into array.
  3. 
