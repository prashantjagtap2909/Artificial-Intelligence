### A* Algorithm:
The A* algorithm is a widely used search algorithm in artificial intelligence that combines the best features of uniform cost search and greedy search algorithms. A* uses a heuristic function to guide the search towards the optimal solution while also considering the cost of reaching that solution.

#### Algorithm:

  - Initialize open and closed sets with the start node as the only member of the open set.
  - While the open set is not empty, select the node with the lowest f(n) value, where f(n) = g(n) + h(n) and g(n) is the cost of the path from the start node to n, and h(n) is the heuristic estimate of the cost from n to the goal.
  - If the selected node is the goal node, then return the path to the goal.
  - For each successor of the selected node, calculate its g and h values, and add it to the open set if it is not already there or if the new g value is lower than the previous one.
  - Move the selected node from the open set to the closed set.


#### Performance Evaluation:
A* algorithm is complete, optimal, and admissible, meaning that it will always find the optimal solution if one exists, and it will never overestimate the cost to the goal. A* performs well when the heuristic function is well-designed, as it can quickly find the optimal solution without expanding too many nodes. However, A* can be slow when the search space is very large or when the heuristic is not informative.
