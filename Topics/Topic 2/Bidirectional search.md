### Bidirectional Search:
Bidirectional search is a type of search algorithm that explores the search space from both the initial state and the goal state simultaneously. It is a useful algorithm in situations where the search space is too large, and the goal state is far from the initial state. Bidirectional search reduces the time and memory complexity of the search process by exploring the search space from both ends.
![image](https://user-images.githubusercontent.com/93985255/230156542-cda91c21-ee80-4157-976a-60ead0f74faf.png)


#### Algorithm:

  - Initialize the search tree with the initial state and the goal state.
  - While neither search has found the goal state, expand the search from both ends simultaneously.
  - If a state is reached from both searches, a solution has been found.
  - Return the path from the initial state to the common state and from the goal state to the common state.


#### Performance Evaluation:
Bidirectional search is a useful algorithm in situations where the search space is large and the goal state is far from the initial state. It reduces the search time and memory requirements by exploring the search space from both ends. However, it requires additional memory to store both the search trees and may not be feasible for large search spaces.
