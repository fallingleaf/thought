## Graph

**Definition**

- Graph is data structure with nodes and edges.
- Graph has 2 types: directed and undirected (no direction)
- Graph problems are usually subtle as they are not stated clearly, and often
need to convert data to graph edges and nodes.

**Graph Transversal**

1. Graph can transverse in both DFS and BFS ways:
    - Undirected graph: store visited node when transverse, if node in visited,
    graph has cycle
    - Directed graph: use hash map for node status, initial status is undiscovered
        - BFS: put a undiscovered node in queue and set it as discovered, pop a
        node from queue and set it as processed, put all of its neighbors to queue
        - DFS: put a undiscovered node in queue and set it as discovered, check
        its neighbors, if neighbor is discovered then there's cycle, otherwise
        recursively process neighbor, set its status to processed.

2. Application:
    - BFS: use to find shortest distance in undirected graph
    - DFS: use to detect cycle in directed graph and topological sort

**Question**

- Course schedule: given list of courses and their prerequisites, find other of
courses. Graph data: convert courses as nodes and prerequisites as neighbor
list. Run topological sort on graph, graph can be disconnected, therefore need to
run DFS for all nodes.

- Alien dictionary: given sorted list of words, find the order of characters.
Observe that words are sorted by their characters, 2 adjacent words chars can form
a directed edge in graph, use these edges to run topological sort for chars.

- Bus routes: each bus has list of stops, find minimum number of buses from first
stop to end stop.
    - We can analyze that user can go from this bus to other bus if
    2 buses share one or more stop.
    - Use this information, we can form an undirected edges for a list of buses.
    However, how to find which use to travel?
    - Check all buses if they have start and end point. We can run BFS from buses 
    that have start point to buses have end point.
