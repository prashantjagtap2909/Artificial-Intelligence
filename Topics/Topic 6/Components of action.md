### Components of representing action

- In classical planning, representing actions involves capturing the essential components and characteristics of actions in a formal manner. These components provide the necessary information for planning algorithms to reason about actions and generate a sequence of actions to achieve a desired goal. 
 
- The three key components of representing actions in classical planning are preconditions, effects, and action costs. 

1. Preconditions:
   Preconditions describe the conditions that must be satisfied for an action to be applicable or executable. They specify the state of the world that must hold before the action can be performed. Preconditions act as constraints that determine whether an action can be taken or not.

   Example: Consider a planning problem where the goal is to make a cup of tea. An example precondition for the action "boil water" could be "there is water available in the kettle." This means that the action can only be executed if there is water in the kettle beforehand.

2. Effects:
   Effects describe the changes or modifications that occur in the state of the world after an action is executed. They represent the consequences or outcomes of performing an action and capture the changes in the state variables or propositions that are affected by the action.

   Example: Continuing with the tea-making example, the effect of the action "boil water" could be "the water in the kettle becomes hot." This effect updates the state of the world by changing the value of the state variable "temperature of water" from "cold" to "hot."

3. Action Costs:
   Action costs represent the numerical values assigned to actions to indicate their associated costs or expenses. These costs can represent various factors such as time, resources, energy, or any other relevant measure. The action costs are used by planning algorithms to optimize plans by considering the overall cost of executing a sequence of actions.

   Example: In a planning problem involving travel, an action "drive from city A to city B" may have a cost associated with it, representing the distance or time required for the journey. The cost can be measured in kilometers or minutes, and planning algorithms can aim to find the plan with the lowest total cost.

