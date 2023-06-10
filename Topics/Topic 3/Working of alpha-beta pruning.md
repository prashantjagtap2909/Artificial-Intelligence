### Working of Alpha-Beta Pruning:


- Step 1: At the first step the, Max player will start first move from node A where α= -∞ and β= +∞, these value of alpha and beta passed down to node B where again α= -∞ and β= +∞, and Node B passes the same value to its child D.
![image](https://github.com/prashantjagtap2909/Artificial-Intelligence/assets/93985255/54df71c0-9369-4ff0-9544-0f37f2bc3dba)


- Step 2: At Node D, the value of α will be calculated as its turn for Max. The value of α is compared with firstly 2 and then 3, and the max (2, 3) = 3 will be the value of α at node D and node value will also 3.



- Step 3: Now algorithm backtrack to node B, where the value of β will change as this is a turn of Min, Now β= +∞, will compare with the available subsequent nodes value, i.e. min (∞, 3) = 3, hence at node B now α= -∞, and β= 3.


![image](https://github.com/prashantjagtap2909/Artificial-Intelligence/assets/93985255/da57107a-e800-4afb-a9b0-06c5c561d9fd)

   In the next step, algorithm traverse the next successor of Node B which is node E, and the values of α= -∞, and β= 3 will also be passed.

- Step 4: At node E, Max will take its turn, and the value of alpha will change. The current value of alpha will be compared with 5, so max (-∞, 5) = 5, hence at node E α= 5 and β= 3, where α>=β, so the right successor of E will be pruned, and algorithm will not traverse it, and the value at node E will be 5.

![image](https://github.com/prashantjagtap2909/Artificial-Intelligence/assets/93985255/ffd5998a-8450-4eee-8ee0-2f889989097d)


- Step 5: At next step, algorithm again backtrack the tree, from node B to node A. At node A, the value of alpha will be changed the maximum available value is 3 as max (-∞, 3)= 3, and β= +∞, these two values now passes to right successor of A which is Node C.

    At node C, α=3 and β= +∞, and the same values will be passed on to node F.

- Step 6: At node F, again the value of α will be compared with left child which is 0, and max(3,0)= 3, and then compared with right child which is 1, and max(3,1)= 3 still α remains 3, but the node value of F will become 1.


![image](https://github.com/prashantjagtap2909/Artificial-Intelligence/assets/93985255/0e24d973-54d0-4d2f-958e-d2483c19f369)


- Step 7: Node F returns the node value 1 to node C, at C α= 3 and β= +∞, here the value of beta will be changed, it will compare with 1 so min (∞, 1) = 1. Now at C, α=3 and β= 1, and again it satisfies the condition α>=β, so the next child of C which is G will be pruned, and the algorithm will not compute the entire sub-tree G.

![image](https://github.com/prashantjagtap2909/Artificial-Intelligence/assets/93985255/30f08672-2163-4004-b804-468e9a6d5794)


- Step 8: C now returns the value of 1 to A here the best value for A is max (3, 1) = 3. Following is the final game tree which is the showing the nodes which are computed and nodes which has never computed. Hence the optimal value for the maximizer is 3 for this example.


![image](https://github.com/prashantjagtap2909/Artificial-Intelligence/assets/93985255/59588d29-83f2-4618-907d-c0567e34c0fc)


