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
