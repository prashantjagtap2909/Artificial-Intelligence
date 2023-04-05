### Iterative Deepening Search (IDS):
IDS is a blind search algorithm that combines the advantages of BFS and DFS. It performs DFS up to a certain depth limit, and then starts over with a higher depth limit if the goal state is not found. IDS guarantees that the shortest path from the initial state to the goal state will be found first. The performance of IDS depends on the branching factor of the problem and the depth of the goal state.


#### Algorithm:

  - Set the depth limit to 0.
  - Repeat the following steps:
    - a. Perform DFS up to the current depth limit.
    - b. If the goal state is found, return the path from the initial state to the goal state.
    - c. Increment the depth limit.
  - Return failure if the depth limit exceeds the maximum depth.


#### Performance Evaluation:
The time complexity of IDS is O(b^d), where b is the branching factor of the problem and d is the depth of the goal state. The space complexity of IDS is O(bd), as it stores all the nodes along the path from the root to the current node.
