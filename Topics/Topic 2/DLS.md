### Depth-Limited Search:
Depth-limited search is a type of search algorithm that limits the search depth to a predefined level. It is a variation of depth-first search that avoids infinite loops and explores the most promising nodes first. The algorithm starts at the initial state and explores all possible paths of a given length before moving to the next level. If the goal state is not found at the specified depth, the algorithm backtracks and explores other paths. The algorithm terminates when the goal state is found or all possible paths have been explored up to the predefined depth limit.


#### Algorithm:

  - Initialize the search tree with the initial state.
  - If the current state is the goal state, return the path to the goal state.
  - If the current depth limit has been reached, return failure.
  - For each possible action from the current state, generate a new state.
  - Recursively apply the algorithm to the new state with an incremented depth limit.
  - If the goal state is found, return the path to the goal state.


#### Performance Evaluation:
Depth-limited search is useful in situations where the search space is large, and the goal state is deep within the search space. It is a memory-efficient algorithm that can find solutions quickly if the goal state is not too deep. However, if the goal state is beyond the specified depth limit, the algorithm will not find a solution.
