### Regression planner
- A regression planner is a type of planning algorithm that works backward from the goal state to the initial state by recursively decomposing the goal into subgoals and generating a plan to achieve each subgoal. It is based on the idea of regression, where the planner analyzes the preconditions and effects of actions in reverse, starting from the goal state and recursively moving backward until reaching the initial state.
- The regression planner works backward from the goal state, decomposing complex goals into simpler subgoals and generating plans to achieve them. It utilizes the preconditions and effects of actions to determine the necessary sequence of actions to achieve each subgoal. The recursive nature of the algorithm allows for the decomposition and generation of plans at multiple levels, effectively breaking down the overall goal into achievable steps.

### Algorithm:

1. Input:
   - Initial state: The current state of the world.
   - Goal state: The desired state that the planner aims to achieve.
   - Set of actions: The available actions with their preconditions and effects.

2. Recursive Regression:
   - If the current state is the goal state, return an empty plan as the goal is already satisfied.
   - Otherwise, select a goal substate from the unachieved subgoals in the goal state.

3. Decomposition:
   - Find an action whose effect matches the goal substate.
   - If such an action exists, add it to the plan and proceed to the next unachieved subgoal.
   - If no matching action is found, perform the following steps:

     a. Decompose the goal substate into simpler subgoals.
     
     b. For each subgoal, recursively apply the regression planner algorithm to generate a plan to achieve the subgoal.
     
     c. Merge the subplans obtained from the recursive calls into a single plan.
     
     d. Add the necessary actions to the plan to achieve the current goal substate.
     
     e. Proceed to the next unachieved subgoal.

4. Return Plan:
   - Once all goal substates are achieved, return the generated plan.


