### Depth-First Search (DFS):
DFS is a blind search algorithm that explores the problem space in a depth-first manner, i.e., it explores as far as possible along each branch before backtracking. The algorithm maintains a stack to keep track of the nodes that need to be expanded, and it visits each node only once. DFS does not guarantee that the shortest path from the initial state to the goal state will be found first. The performance of DFS depends on the depth of the goal state and the branching factor of the problem.


#### Algorithm:

  - Initialize the stack with the initial state.
  - While the stack is not empty:
    - a. Pop the next state from the stack.
    - b. If the state is the goal state, return the path from the initial state to the goal state.
    - c. Generate all possible successor states of the current state.
    - d. Push the successor states onto the stack.
  - Return failure if the stack is empty.

#### Performance Evaluation:
The time complexity of DFS is O(b^m), where b is the branching factor of the problem and m is the maximum depth of the tree. The space complexity of DFS is O(bm), as it stores all the nodes along the path from the root to the current node.
