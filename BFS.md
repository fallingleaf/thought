## BFS

**Definition**

- BFS is technique that processes all nearest elements first before going deeper.

**Usage**

- Most of problems using DFS to find all possible values can be solved by BFS.
- Because the nature of BFS is to process nearest first, it can optimally be
used to find minimum path.
  - Shortest distance to houses: do BFS from each house and record sum distance
  for each empty cell as well as number of houses it can reach.
  - Knight move in chess board: find min step to reach x, y on board; use BFS
  for 8 possible moves and also track visited location to avoid duplicate
  - Wall and gate: find minimum distance from empty cell to gate, put all gates
  into queue, and do BFS from each gate to empty cell to update distance
  - Jump game II: find minimum of jumps to reach destination, use BFS to calculate
  the maximum next location for all points in current reach.
  - Word Ladder II: find shortest transformation from one begin word to end word,
  use BFS from begin word to all possible words in dictionary, also need to cache
  distance from begin word to next word, if longer than we don't need to try that
  word.
  - Race car: car can accelerate or reverse speed, find min step to reach destination,
  use BFS for next location and speed, store (location, speed) as visited node

**Notes**

- Same as DFS, it needs to keep track of visited nodes to avoid duplicate in BFS 
