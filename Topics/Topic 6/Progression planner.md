### Progression planner

- A progression planner is a type of planning algorithm that constructs a plan by progressively refining an initial state until the desired goal state is reached. It works by iteratively applying action operators to the current state, generating new states, and searching for a sequence of actions that transforms the initial state into the goal state. The algorithm follows a systematic process to explore the state space and build a plan incrementally.
- The progression planner explores the state space by repeatedly applying available actions and generating new states. It continues this process until it reaches the goal state. The planner may employ various search strategies, such as depth-first search or breadth-first search, to navigate the state space efficiently and find a plan.

- The algorithm relies on the availability of action operators, which describe the actions that can be performed and their preconditions and effects. These operators define the valid state transitions and guide the planner's decision-making process.

- The progression planner algorithm does not backtrack or undo actions once they are applied. It proceeds forward, incrementally refining the state until the goal is achieved. This approach makes the algorithm efficient for planning problems where the state space is not too large and the goal can be reached through a sequence of feasible actions.
### Algorithm

1. Input:
   - Initial state: Represents the starting state of the planning problem.
   - Goal state: Represents the desired state to be achieved.

2. Initialize:
   - Create an empty plan.

3. While the current state is not the goal state:
     - Apply available action operators to the current state.
     - Generate new states by applying the actions, considering their preconditions and effects.
     - Select one of the new states as the next current state.

4. Generate the plan:
   - Once the goal state is reached, trace back the sequence of actions taken from the initial state to the goal state.
   - This sequence of actions forms the plan.
