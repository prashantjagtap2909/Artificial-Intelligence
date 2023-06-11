### Partial order planning

- Partial order planning is a type of planning algorithm that allows for the parallel execution of actions and represents the dependencies and constraints between actions using a partial order. Unlike total order planning, where actions are strictly ordered, partial order planning offers more flexibility by allowing actions to be executed concurrently when there are no interdependencies or conflicts.

- In partial order planning, the planning process involves constructing a partial order plan, which is a directed acyclic graph (DAG) representing the dependencies between actions. Each node in the graph represents an action, and the edges between nodes indicate the ordering constraints or causal relationships between actions.


- In partial ordered planning (POP), ordering of the actions is partial. Also partial ordered planning don’t specify which action will come first out of the two actions which are placed.

- With partial ordered planning, problem can be decomposed, so it can work well in case the environment is non-cooperative.

- It combines two action sequence:

  i. First branch covers left sock and left shoe.

  ii. In case, to wear a left shoe, wearing left sock is precondition, similarly.

  iii. Second branch covers right shock and right shoe.

  iv. Here, wearing a right shock is precondition for wearing the right shoe.

  Once these actions are taken we achieve our goal and reach the finish state.

E.g. Partial order planning of Wearing Shoe

![image](https://github.com/prashantjagtap2909/Artificial-Intelligence/assets/93985255/97362424-610f-4747-8cf4-4cf2b7c56574)



- Pop as search problem:

- Set of actions:

- These are the steps of plan.

- For e.g.: Set of Actions = {Start, Rightsock, Rightshoe ,Leftsock, Leftshoe, Finish}

- Set of ordering constraints/preconditions:

    i. Preconditions are considered as ordering constraints.(i.e. without performing action “x” we cannot perform action “y”)

    ii. For e.g.: Set of ordering = {Right-sock <right-shoe; left-sock<left-shoe}="" that="" is="" in="" order="" to="" wear="" shoe,="" first="" we="" should="" wear="" a="" sock.<="" p="">

- Set of causal links:

- Action A achieves effect “E” for action B

![image](https://github.com/prashantjagtap2909/Artificial-Intelligence/assets/93985255/8a442eab-6e20-4321-b1f6-2d6c591637ec)

   i. You can understand that if you buy an apple its effect can be eating an apple and the precondition of eating an apple is cutting apple.

   ii. For e.g. Set of Causal Links = {Right-sock-> Right-sock-on

Set of open preconditions:

   i. Preconditions are called open if it cannot be achieved by some actions in the plan.

   ii. Consistent Plan is a Solution for POP Problem

   iii. A consistent Plan doesn’t have cycle of constraints; it doesn’t have conflicts in the causal links and doesn’t have open preconditions so it can provide a solution for POP problem.
