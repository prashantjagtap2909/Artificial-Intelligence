### Handling indeterminacy
- Handling indeterminacy refers to addressing situations in which the outcome or state of the world is uncertain or cannot be determined with certainty. It is a crucial aspect of planning and decision-making, as many real-world scenarios involve inherent uncertainties, incomplete information, or stochastic elements.

#### Types of planning methods commonly used to address indeterminacy:

1. Probabilistic Planning:
   Probabilistic planning takes into account the uncertainty in the environment by incorporating probabilistic models. It represents the uncertainty using probabilities and generates plans that maximize expected utility or achieve goals with a certain level of confidence. Probabilistic planning algorithms, such as Markov Decision Processes (MDPs) or Partially Observable Markov Decision Processes (POMDPs), explicitly consider the probabilities of different outcomes and make decisions based on expected outcomes.

2. Reactive Planning:
   Reactive planning focuses on real-time decision-making in dynamic environments. Instead of generating a complete plan in advance, reactive planners continuously monitor the environment and react to the immediate circumstances. These planners use sensory inputs to perceive the current state and select actions based on predefined rules or heuristics. Reactive planning is useful when there is a need for quick responses to changing conditions but may not optimize long-term objectives.

3. Hierarchical Planning:
   Hierarchical planning decomposes complex tasks into a hierarchy of subtasks, each with its own planning process. This approach allows for different levels of abstraction and flexibility to handle indeterminacy. The higher-level plan provides a coarse-grained structure, while lower-level plans address the details and uncertainties. Hierarchical planning helps manage complexity and adapt to changing conditions by allowing different levels of planning to operate independently or interactively.

4. Online Planning:
   Online planning involves generating plans incrementally while the agent is executing actions. It continuously updates and revises the plan based on the current state and the observed outcomes. Online planning methods adapt to new information and dynamically adjust the plan to handle indeterminacy. These planners take into account the changing environment and update their strategies based on real-time feedback.

5. Learning-based Planning:
   Learning-based planning methods employ machine learning techniques to handle indeterminacy. They learn from historical data or interactions with the environment to improve decision-making and generate better plans. Reinforcement learning, for example, enables an agent to learn an optimal policy through trial-and-error interactions with the environment. Learning-based planning methods adapt to uncertainties by leveraging past experiences and continuously improving their decision-making capabilities.

6. Robust Planning:
   Robust planning aims to generate plans that can handle various possible outcomes or disturbances. It considers worst-case scenarios and generates plans that work reasonably well in a wide range of possible situations. Robust planning methods optimize plans to minimize the impact of uncertainties, ensuring that the plans remain effective even if the actual outcomes deviate from the expected ones.

