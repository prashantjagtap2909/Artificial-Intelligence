### Conditioanl planning
- Conditional planning is a type of planning that involves generating plans based on conditions or contingent events. It allows for the construction of plans that can adapt and change depending on the state of the world or the occurrence of certain events. Conditional planning takes into account the uncertainty and unpredictability of the environment and provides a way to handle different scenarios.

- In conditional planning, plans are constructed using a combination of actions and conditional statements that specify what actions to take depending on the observed or anticipated conditions. These conditions can be represented using logical expressions, propositions, or other forms of knowledge representation.


#### Example to illustrate conditional planning:

- Let's consider a simple planning scenario where a robot needs to navigate through a maze to reach a goal location. The robot has the following actions available:

  1. Move Forward
  2. Turn Left
  3. Turn Right

- Now, the robot needs to generate a plan to reach the goal, but the maze may contain walls or obstacles that it needs to avoid. Conditional planning allows the robot to handle these obstacles dynamically.

- Here's a possible conditional plan:

  1. If there is an obstacle ahead, turn left.
  2. If there is no obstacle ahead, move forward.
  3. Repeat steps 1 and 2 until the goal is reached.

- In this plan, the robot checks for the presence of an obstacle ahead at each step and adjusts its actions accordingly. If there is an obstacle, it turns left to avoid it. If there is no obstacle, it moves forward. The plan repeats these steps until the goal is reached, adapting to the changing conditions of the maze.

- The conditional statements in the plan act as decision points, allowing the robot to make choices based on the current state of the environment. These condition-action pairs provide the flexibility for the robot to dynamically adjust its plan and respond to different situations, such as the presence of obstacles or changes in the maze layout.

- Conditional planning is valuable in situations where the environment is uncertain, dynamic, or subject to change. It enables agents to generate plans that can adapt and respond to varying conditions, ensuring robustness and flexibility in achieving desired objectives.
