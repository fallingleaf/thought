## DFS

**Definition**
- DFS is a technique to process deeper nodes first until cannot process anymore,
used to find longest path, exist object or to detect cycle in graph.

**Usage**

- Find all possible values:
  - Find longest increasing path in matrix: try all adjacent cells to make longer path
  - Maximum vacation: try different flights and update maximum vacation days
  - Remove invalid parentheses: remove parentheses at on location, and try DFS
  to remove next invalid location
  - Word break II: return all possible word list for each breaking point
  - Palindrome Partition: find all possible partition at current string
  - Coin exchange: exchange one currency to different currency, use DFS to try all
  currency that can convert

- Pre-process connected nodes:
  - Surrounded regions: use DFS to flip all O connected to O at edge
  - Number of islands: use DFS to mark all lands within same island

- Topological sort: find the order of nodes that satisfies some order constraint
  - Course schedule: course have some prerequisites, present it as edge of graph
  use DFS to sort these courses
  - Alien Dictionary: compare each character in 2 adjacent sorted words, preset
  order of 2 chars as an edge in graph, use topological sort to find out all orders


**DFS vs Backtracking**

- Backtracking is similar approach to DFS, except that it needs to restore previous
state of visited node, before trying new path.
- For example: sudoku solver: try each empty cell with value from 1 to 9, if it
does not solve then reset cell to empty.
- Robot cleaning room (or mouse in maze): after trying one directions, it needs to
go back to previous location by turning 180 degree (2 turn left), then move back,
then turning 180 degree to have same direction. Use a hash set to store visited nodes,
(can assume first location is at 0, 0) move left, right, top, down will increase
or decrease x, y coordination.

**Notes**

- Sometime need to keep track of which node already visited in DFS to avoid duplicate
works.
- Cache result as visiting along the nodes to reduce runtime complexity, for example
longest increasing path problem, we can cache the longest path at each cell to avoid
compute for that cell again.
