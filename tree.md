## Tree

**Definition**

- Tree is data structure like undirected graph but there's no cycle.
- Binary tree is tree with 2 children at most.

**Transversal**

- Tree can transverse in some ways:
  - Pre-order transversal: root -> left -> right
  - In-order transversal: left -> root -> right
  - Post-order transversal: left -> right -> root
  - Level order: use queue to process level by level
  - Vertical order: store index x, y, left child x - 1, y + 1, right child x + 1, y + 1

- Interactive transversal could be done using [Stack](./stack.md)

**Problems**

- Most of tree problems involve transversing and recursively calculate all child nodes.

1. Transversal
  - Serialize and deserialize tree: use pre-order transverse to concat node value
  into string buffer.

  - BST tree iterator: same as in-oder transversal, but with condition, when
  calling next(), pop one node from stack and take right node to put all left nodes
  into stack.

  - Kth smallest: use in-order transversal, decrease K when process root, until
  k equal 0, return value.

  - Right side view: use level order, at each level return right most node.

  - Vertical order
  - Boundary transversal: observe that the boundary of tree includes left side,
  leaves and right side (bottom up)

2. Recursive: assume that has result from both left and child, think about how to form final
result from child nodes data? and which information return from child need to calculate?

  - Longest consecutive: if we have both longest length from both left and right,
  then we just need compare left, right value to current node value, if it's consecutive
  increase length + 1, otherwise reset to 1, update answer along the way.

  - Lowest common ancestor of two nodes p, q:
    - 2 cases:
      - p, q on same left or right of current node, ancestor should be child node
      of that subtree.
      - p, q on left and right subtree of current node, current node is ancestor
    - What to return:
      - if node equals p or q, just need to return itself.
      - find p, q on left and right and check above condition.

  - Maximum path sum: assume we have max path up to left and right, calculate
  result: max of node value + left + right, node value + left, node value + right,
  node value.
    - What to return for child: max of node value + left, node value + right,
    or node value.

  - Count number of nodes in complete tree: simple way to solve it is to count
  left and right.
    - However, it can be optimized, given the definition of complete
  tree, that all level are full except last level, nodes are far left.
    - At least left or right subtree of current node is full and number
    of nodes equal 2^height - 1.
    - If we check left height = right height, then sub tree is full.
