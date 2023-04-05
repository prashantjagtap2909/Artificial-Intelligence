### Breadth-First Search (BFS):
BFS is a blind search algorithm that explores the problem space in a breadth-first manner, i.e., it expands all the nodes at the current level before moving to the next level. The algorithm maintains a queue to keep track of the nodes that need to be expanded, and it visits each node only once. BFS guarantees that the shortest path from the initial state to the goal state will be found first. The performance of BFS depends on the branching factor of the problem, as it explores all the nodes at each level before moving to the next level.

![image](https://user-images.githubusercontent.com/93985255/230155281-087ef0fa-101b-434f-a85a-c8ad2587710b.png)


#### Algorithm:

  - Initialize the queue with the initial state.
  - While the queue is not empty:
    - a. Dequeue the next state from the queue.
    - b. If the state is the goal state, return the path from the initial state to the goal state.
    - c. Generate all possible successor states of the current state.
    - d. Enqueue the successor states onto the queue.
  - Return failure if the queue is empty.

#### Performance Evaluation:
The time complexity of BFS is O(b^d), where b is the branching factor of the problem and d is the depth of the goal state. The space complexity of BFS is also O(b^d), as it stores all the nodes at each level.
