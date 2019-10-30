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

  3. Maximum 3 non-overlap sub array sum of size K:
    - Simple method is to calculate sum of size K at each index and loop to find
    maximum sum.
    - Observe that: mid subarray at i index, left subarray would be at most
    i - K, third at i + K. We could pre-calculate max from left and from right for left
    and right subarray.

  4. Product array except self:
    - Find product at each number except itself
    - We could run 2 loops to multiply left and right part => repeated work
    - Use 1 array to store right product up to index i

**Caching Data**
- Caching or memorize data is technique to reduce repeating work.
- Cache processed node results when solving maximum or minimum problem to avoid
processing this node again, usually apply for some BFS or DFS strategy.

**Solve Complex Problem**
- Break down problem into smaller, simple sub-problems
  1. Parse Lisp Expression: expression has 3 operations: add, mult and let, we
  can break problem into solving each operation
    - For "add": it has 2 children e.g (add 1 10), (add 10 x), (add 1 (mul x 4))
    can recursively evaluate each children then add them.
    - Same for "mult" operation
    - For "let": e.g "let x 1 y (add 5 x) (mul x y)", it has 2 pairs: x 1,
    y (add 5 x) and final expression: (mul x y), we can evaluate value in each pair,
    assign it to scope for solving last expression.
    - Last issue is how to parse expression for each operation: e.g (add x (mul 3 y))
    when we encounter operation e.g "add", parse remain token from next "space",
    and we want sub-expression as one child, count open and close parentheses,
    if count = 0 or space, add it as 1 child.
