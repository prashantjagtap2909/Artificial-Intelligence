### WAlkSAT algorithm
- WalkSAT is a local search algorithm for solving Boolean satisfiability problems (SAT). It works by randomly assigning values to variables and then iteratively flipping the values of variables that violate clauses until a satisfying assignment is found.

### Characteristics:

- It is a local search algorithm, which means that it only considers a small number of variables at a time.
- It is a randomized algorithm, which means that it does not guarantee to find a satisfying assignment.
- It is a heuristic algorithm, which means that it is not guaranteed to find the optimal solution.

### Example

Given the SAT formula:

(x1 or x2 or x3) and (not x1 or not x2 or x4) and (not x1 or x2 or not x5)

The WalkSAT algorithm might start by randomly assigning the values true to x1, x2, and x3. This assignment does not satisfy the formula, so the algorithm would then flip the value of x1 to false. This new assignment satisfies the first two clauses, but it violates the third clause. The algorithm would then flip the value of x2 to true. This new assignment satisfies all three clauses, so the algorithm terminates.

The WalkSAT algorithm is a simple and efficient algorithm for solving SAT problems. However, it is not guaranteed to find the optimal solution. In some cases, it may find a local minimum that is not a global minimum.
