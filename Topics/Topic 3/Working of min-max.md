### Working of Min-Max Algorithm:
- The working of the minimax algorithm can be easily described using an example. Below we have taken an example of game-tree which is representing the two-player game.
- In this example, there are two players one is called Maximizer and other is called Minimizer.
- Maximizer will try to get the Maximum possible score, and Minimizer will try to get the minimum possible score.
- This algorithm applies DFS, so in this game-tree, we have to go all the way through the leaves to reach the terminal nodes.
- At the terminal node, the terminal values are given so we will compare those value and backtrack the tree until the initial state occurs. Following are the main steps involved in solving the two-player game tree:

#### Example:- 

- Step-1: In the first step, the algorithm generates the entire game-tree and apply the utility function to get the utility values for the terminal states. In the below tree diagram, let's take A is the initial state of the tree. Suppose maximizer takes first turn which has worst-case initial value =- infinity, and minimizer will take next turn which has worst-case initial value = +infinity.
![image](https://github.com/prashantjagtap2909/Artificial-Intelligence/assets/93985255/ea5d23ae-ff14-41eb-8af8-d79c2dc004a9)


- Step 2: Now, first we find the utilities value for the Maximizer, its initial value is -∞, so we will compare each value in terminal state with initial value of Maximizer and determines the higher nodes values. It will find the maximum among the all.



![image](https://github.com/prashantjagtap2909/Artificial-Intelligence/assets/93985255/43a904f2-7456-41bb-95e0-ac702115f3fb)

- Step 3: In the next step, it's a turn for minimizer, so it will compare all nodes value with +∞, and will find the 3rd layer node values.

![image](https://github.com/prashantjagtap2909/Artificial-Intelligence/assets/93985255/ee5ccea1-dd05-4ed2-962c-9ce7c2aa462b)


- Step 4: Now it's a turn for Maximizer, and it will again choose the maximum of all nodes value and find the maximum value for the root node. In this game tree, there are only 4 layers, hence we reach immediately to the root node, but in real games, there will be more than 4 layers.


![image](https://github.com/prashantjagtap2909/Artificial-Intelligence/assets/93985255/317bf3dd-4d44-4ad7-a03e-593516cdda98)

That was the complete workflow of the minimax two player game.
