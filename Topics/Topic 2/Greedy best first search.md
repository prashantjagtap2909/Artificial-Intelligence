### Greedy Best-First Search:
Greedy best-first search is a type of best-first search algorithm that chooses the next state based only on the heuristic value, without considering the actual cost of reaching that state. Greedy best-first search is a type of greedy algorithm and can be less efficient than more complex search algorithms, as it does not always choose the optimal path.



#### Algorithm:

  - Initialize the search with the initial state
  - Generate the possible next states from the current state
  - Calculate the heuristic value for each possible next state
  - Choose the next state with the lowest heuristic value
  - Repeat steps 2-4 until the goal state is reached or no more states can be generated


#### Performance Evaluation:
Greedy best-first search can be a fast and simple algorithm for problems with simple and easy-to-calculate heuristic functions. However, it can be less efficient than more complex search algorithms such as A* search, as it does not take into account the actual cost of reaching the current state.
