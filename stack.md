## Stack

**Definition**
- Stack is data structure that supports First in Last out.

**Usage**
- Use stack to compare current value with previous value store in stack, e.g
  - Valid parentheses problem: use stack to store open parentheses, if see close
  parentheses, check if previous token in stack is open parentheses
  - Largest rectangle area in histogram: if columns are blocked by later smaller
  column, we don't need to process. Use stack to store higher column, compare current
  column with previous column if smaller remove from stack and calculate area.
  - Maximum sliding window: find maximum value in window K size. When we see new number
  in current window that larger than previous one, we don't need to keep previous
  number. Use double queue to store value in decreasing order.

- Use stack to store temporary data from last computation (without the need to recursive)
  - Binary tree - pre-order transversal: root -> left -> right.
  Init stack with root node, pop one node from stack, because left node need to
  process before right node, so push its right node, its left node
  - Binary tree - in-order transversal: left -> root -> right.
  Push all left nodes to stack, pop one node to process, take its right node
  and repeat above process.
  - Binary tree - post-order transversal: left -> right -> root
  Init stack with root node. Use prev to track process direction. If current node
  is left or right child of prev node, process down more, pushing left (if exists)
  or right node to stack. If prev node is left or right child of current node,
  check if right node process, move up (pop from stack)

  - Basic calculator with parentheses: when encounter open parentheses, use stack
  to store previous result and sign instead of calling recursively to compute value
  in parentheses.
  - K smallest values in binary search tree: use 2 stacks to store smaller and
  larger values to target. Why stack but not queue? Because as we transverse down
  the values see closer to target than previous nodes. Therefore, they should be
  consider first.

- Use stack to reverse order
  - Plus 2 numbers in linked list (most significant first):
  instead of reverse linked list and calculate, push node values from linkedlist
  to stack to calculate.
  - Course schedule: (topological sort) 



**Question**