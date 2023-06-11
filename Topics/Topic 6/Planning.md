### Planning
- Planning in AI is the process of finding a sequence of actions that will achieve a desired goal. It is a subfield of artificial intelligence that is concerned with the development of algorithms that can automatically generate plans.


### Types of Planning


1. Forward State Space Planning (FSSP)
- FSSP behaves in the same way as forwarding state-space search. It says that given an initial state S in any domain, we perform some necessary actions and obtain a new state S' (which also contains some new terms), called a progression. It continues until we reach the target position. Action should be taken in this matter.

- Disadvantage: Large branching factor
- Advantage: The algorithm is Sound

2. Backward State Space Planning (BSSP)
- BSSP behaves similarly to backward state-space search. In this, we move from the target state g to the sub-goal g, tracing the previous action to achieve that goal. This process is called regression (going back to the previous goal or sub-goal). These sub-goals should also be checked for consistency. The action should be relevant in this case.

- Disadvantages: not sound algorithm (sometimes inconsistency can be found)
- Advantage: Small branching factor (much smaller than FSSP)

#### Block-world planning problem
- The block-world problem is known as the Sussmann anomaly.
- The non-interlaced planners of the early 1970s were unable to solve this problem. Therefore it is considered odd.
- When two sub-goals, G1 and G2, are given, a non-interleaved planner either produces a plan for G1 that is combined with a plan for G2 or vice versa.
- In the block-world problem, three blocks labeled 'A', 'B', and 'C' are allowed to rest on a flat surface. The given condition is that only one block can be moved at a time to achieve the target.


![image](https://github.com/prashantjagtap2909/Artificial-Intelligence/assets/93985255/e7dd97dd-a333-4055-b04b-a4baddd314d2)

#### The plan includes the following important steps:

- Choose the best rule to apply the next rule based on the best available guess.
- Apply the chosen rule to calculate the new problem condition.
- Find out when a solution has been found.
- Detect dead ends so they can be discarded and direct system effort in more useful directions.
- Find out when a near-perfect solution is found.



##### Target stack plan
- It is one of the most important planning algorithms used by STRIPS.
- Stacks are used in algorithms to capture the action and complete the target. A knowledge base is used to hold the current situation and actions.
- A target stack is similar to a node in a search tree, where branches are created with a choice of action.



#### The important steps of the algorithm 

- Start by pushing the original target onto the stack. Repeat this until the pile is empty. If the stack top is a mixed target, push its unsatisfied sub-targets onto the stack.
- If the stack top is a single unsatisfied target, replace it with action and push the action precondition to the stack to satisfy the condition.
- If the stack top is an action, pop it off the stack, execute it and replace the knowledge base with the action's effect.


- If the stack top is a satisfactory target, pop it off the stack.

##### Non-linear Planning
- This Planning is used to set a goal stack and is included in the search space of all possible sub-goal orderings. It handles the goal interactions by the interleaving method.

- Advantages of non-Linear Planning


  - Non-linear Planning may be an optimal solution concerning planning length (depending on the search strategy used).

- Disadvantages of Nonlinear Planning

  - It takes a larger search space since all possible goal orderings are considered.

  - Complex algorithm to understand.

- Algorithm

  - Choose a goal 'g' from the goal set
  - If 'g' does not match the state, then
  - Choose an operator 'o' whose add-list matches goal g
  - Push 'o' on the OpStack
  - Add the preconditions of 'o' to the goal set
  - While all preconditions of the operator on top of OpenStack are met in a state
  - Pop operator o from top of opstack
  - state = apply(o, state)
  - plan = [plan; o]
