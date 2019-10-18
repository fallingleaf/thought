## Union find

**Definition**
- Union Find or Disjoint Set is data structure that keeps track of a set of elements
partitioned in number of disjoint subsets.

- Union-find has 2 steps:
    - Find: determine which subset element is in, by finding its parent recursively
    - Union: join 2 subsets into one single subset, by setting parent of one
    subset as parent of other, so that they have same parent


**Usage**
- Union-find used to find cycle in undirected graph
    - Redundant connection: find redundant edge u, v; if cannot union u and v
    return it

    - Graph valid tree: check if graph has cycle using union find
