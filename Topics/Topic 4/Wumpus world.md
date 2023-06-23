### Wumpus World

- The Wumpus World is a classic problem in artificial intelligence. It is a simple, yet challenging problem that has been used to study a variety of AI techniques.

- The Wumpus World is a 2D world with a grid of rooms. Each room can be connected to up to four other rooms. The world also contains a wumpus, a pit, and a gold. The wumpus is a creature that lives in one of the rooms. The pit is a hole that will kill the agent if it falls in. The gold is a valuable treasure that the agent must collect.

- The agent's goal is to find the gold and escape the world without being killed by the wumpus or falling in the pit. The agent can move around the world by entering a room. The agent can also shoot an arrow to kill the wumpus.

- The Wumpus World is a challenging problem because the agent cannot see the entire world. The agent can only sense the presence of the wumpus and the pit in adjacent rooms. The agent must use this limited information to infer the location of the wumpus and the pit, and to plan a safe path to the gold.

- The Wumpus World has been used to study a variety of AI techniques, including search, planning, and reasoning. It is a valuable tool for understanding how AI agents can solve complex problems in a world that is not fully observable.


- Following is a sample diagram for representing the Wumpus world. It is showing some rooms with Pits, one room with Wumpus and one agent at (1, 1) square location of the world.


![image](https://github.com/prashantjagtap2909/Artificial-Intelligence/assets/93985255/0db92739-03d5-4c8f-9d68-be3c54f85fcf)


- There are also some components which can help the agent to navigate the cave. These components are given as follows:


  - The rooms adjacent to the Wumpus room are smelly, so that it would have some stench.
  - The room adjacent to PITs has a breeze, so if the agent reaches near to PIT, then he will perceive the breeze.
  -There will be glitter in the room if and only if the room has gold.
  -The Wumpus can be killed by the agent if the agent is facing to it, and Wumpus will emit a horrible scream which can be heard anywhere in the cave.



#### PEAS description of Wumpus world:


##### Performance measure:
- +1000 reward points if the agent comes out of the cave with the gold.
- -1000 points penalty for being eaten by the Wumpus or falling into the pit.
- -1 for each action, and -10 for using an arrow.
- The game ends if either agent dies or came out of the cave.


##### Environment:
- A 4*4 grid of rooms.
- The agent initially in room square [1, 1], facing toward the right.
- Location of Wumpus and gold are chosen randomly except the first square [1,1].
- Each square of the cave can be a pit with probability 0.2 except the first square.



##### Actuators:
- Left turn,
- Right turn
- Move forward
- Grab
- Release
- Shoot.


##### Sensors:
- The agent will perceive the stench if he is in the room adjacent to the Wumpus. (Not diagonally).
- The agent will perceive breeze if he is in the room directly adjacent to the Pit.
- The agent will perceive the glitter in the room where the gold is present.
- The agent will perceive the bump if he walks into a wall.
- When the Wumpus is shot, it emits a horrible scream which can be perceived anywhere in the cave.
- These percepts can be represented as five element list, in which we will have different indicators for each sensor.
- Example if agent perceives stench, breeze, but no glitter, no bump, and no scream then it can be represented as:
[Stench, Breeze, None, None, None].



#### The Wumpus world Properties:
- Partially observable: The Wumpus world is partially observable because the agent can only perceive the close environment such as an adjacent room.
- Deterministic: It is deterministic, as the result and outcome of the world are already known.
- Sequential: The order is important, so it is sequential.
- Static: It is static as Wumpus and Pits are not moving.
- Discrete: The environment is discrete.
- One agent: The environment is a single agent as we have one agent only and Wumpus is not considered as an agent.


#### Exploring the Wumpus world:
- Now we will explore the Wumpus world and will determine how the agent will find its goal by applying logical reasoning.

- Agent's First step:

  - Initially, the agent is in the first room or on the square [1,1], and we already know that this room is safe for the agent, so to represent on the below diagram (a) that room is safe we will add symbol OK. Symbol A is used to represent agent, symbol B for the breeze, G for Glitter or gold, V for the visited room, P for pits, W for Wumpus.

  - At Room [1,1] agent does not feel any breeze or any Stench which means the adjacent squares are also OK.


![image](https://github.com/prashantjagtap2909/Artificial-Intelligence/assets/93985255/922a9b98-c87a-463f-8faa-1eeae74c8642)


- Agent's second Step:

  - Now agent needs to move forward, so it will either move to [1, 2], or [2,1]. Let's suppose agent moves to the room [2, 1], at this room agent perceives some breeze which means Pit is around this room. The pit can be in [3, 1], or [2,2], so we will add symbol P? to say that, is this Pit room?

  - Now agent will stop and think and will not make any harmful move. The agent will go back to the [1, 1] room. The room [1,1], and [2,1] are visited by the agent, so we will use symbol V to represent the visited squares.


- Agent's third step:

  - At the third step, now agent will move to the room [1,2] which is OK. In the room [1,2] agent perceives a stench which means there must be a Wumpus nearby. But Wumpus cannot be in the room [1,1] as by rules of the game, and also not in [2,2] (Agent had not detected any stench when he was at [2,1]). Therefore agent infers that Wumpus is in the room [1,3], and in current state, there is no breeze which means in [2,2] there is no Pit and no Wumpus. So it is safe, and we will mark it OK, and the agent moves further in [2,2].

![image](https://github.com/prashantjagtap2909/Artificial-Intelligence/assets/93985255/2e5d665e-75b3-4e0f-bf9b-7eb9fc08fe84)


- Agent's fourth step:

  - At room [2,2], here no stench and no breezes present so let's suppose agent decides to move to [2,3]. At room [2,3] agent perceives glitter, so it should grab the gold and climb out of the cave.
