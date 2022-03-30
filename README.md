# LeetCodeNotes

## Dynamic Programming 

### 0/1 Knapsack Problem / Decision Making
This problem requires decision at each item. It usually have a constraint or target
#### Key insight:
- It usually has two states 1. number of items available at a particular instance 2. the increasing/decreasing constraint/target capacity.
- Subproblem: given item 1, how can I reach target 1, 2, 3....n. Given item 1 + 2, how can I reach target 1, 2, 3...n. Given item 1 + 2 + 3, how can I reach target 1, 2, 3...n and so on till all items.
- Therefore, the intuition is to memoize or tabulate the two state: 1. number of items we are considering at a particular instance, and then consider more item till all items are considered. 2. for each set of items, how does it contribute to target 1...n.
- Think about it like a game. State 1 is each level, first consider level 1, then level 1 and level 2, then 1,2,3 and so on. At each level, you must make a decision to do something, and depending on what you do, you will contribute to the target / end game aspects differently, and you must consider all the end game aspects for each level because next level will be dependent on last level's endgame aspect. 
- In short: The combination of decisions for 1...all items are considered and their contributions to the target will be recorded.


## DFS vs. Backtracking Algorithm, an Inspiration from the Atlantic Pacific Ocean problem.
- Why bruteforce DFS takes a long time in this case?
- This is becuase you need to visit a node more than once since you are dependent on all sides, this requires unmarking node as visited, it is practice of backtracking!
- Backtracking 

Backtracking is a more general purpose algorithm.
Depth-First search is a specific form of backtracking related to searching tree structures.

Difference 1:
DFS handles an explicit tree.While Backtracking handles an implicit tree

Difference 2:
Depth First Search is a special type of backtracking algorithmic design paradigm where the process of backtracking takes place in the leaf nodes. In case of backtracking,the algorithm also rejects the useless branch of the state-space tree.This is why DFS maintains the entire tree structure while Backtracking maintaines a pruned tree

In Backtracking, we need to restore previous state of visited node, by making visited=false, after exploring current path whereas in DFS the state of the node remains same after a path is explored so that it will not be explored again. Or we can say that pure DFS is a variant of backtracking in which state of visited nodes are not restored, and this variant is only useful for problems related to searching (reachability, etc) and not for problems involving pattern finding, for which we need to use the usual backtracking tree pruning algorithm.
DFS is quicker than a generic backtracking algorithm, due to the reason stated above.
