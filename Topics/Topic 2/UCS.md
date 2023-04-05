### Uniform Cost Search:
Uniform cost search is a type of search algorithm that explores the search space by prioritizing the nodes with the lowest path cost. It is an optimal algorithm that guarantees to find the shortest path from the initial state to the goal state. Uniform cost search is particularly useful in situations where the path cost between states is not uniform.



#### Algorithm:

  - Initialize the search tree with the initial state and a cost of 0.
  - While the search tree is not empty, select the node with the lowest path cost.
  - If the selected node is the goal state, return the path to the goal state.
  - For each possible action from the selected node, generate a new state and calculate its path cost.
  - Add the new state to the search tree with its calculated path cost.
  - Repeat steps 2-5 until the goal state is found.


#### Performance Evaluation:
Uniform cost search is an optimal algorithm that guarantees to find the shortest path from the initial state to the goal state. However, it may not be feasible for large search spaces, as it requires keeping track of the path cost for each state. Additionally, it may be slow in situations where the path cost varies significantly between states.
