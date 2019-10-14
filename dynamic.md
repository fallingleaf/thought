
## Dynamic Programming
**Type 1**
- Current state depends on previous state, find max value
by previous state
- Questions: maximum value, revenue e.g rob cutting, longest increasing subsequence
in array

**Type 2**
- Compare 2 sequences, 2 cases: xi = yj or xi != yj
- Questions: find maximum matching e.g: longest common sequence, palindrome, edit string
distance, longest increasing subsequence.

**Type 3**
- Selection process, at each step, it can either choose xi to be in
collection or dump it
- Questions: maximize the value, or count number of ways e.g: k-snapsack problem,
coin change problem, subset sum to K

**Type 4**
- Partition list into number of subarray that minimize or maximize subarray,
- Questions: partition subarray sum

**Type 5**
- Catalan number, count number of ways: if process x element, then
the remain n-x-1 element could be processed in same way, forming formula:
C(n) = sum C(i) * C(n - i - 1)
- Questions: number of expression for n parenthesis number of full binary tree,
number of tree with n leaves

**Type 6**
- Bell number: count number of ways to partition a set, at element n
it can add to current set or be a single set, S(n+1, k) = k*S(n, k) + S(n, k-1)
k = 1...n
- B(i, j) = B(i-1, i-1) if (j=0) or B(i-1, j-1) + B(i, j-1)
