# 极小极大搜索 minmax search

## 目标

给定一个两人对弈游戏，要求实现极小极大搜索算法，找到最优的下一步走法。

## 基本原理

- 极小极大搜索是一种深度优先搜索算法，它递归地搜索整个游戏树，直到达到叶节点。
- 当达到叶节点时，对于每个玩家，它将计算出一个评估值，表示当前状态的好坏。
- 对于最大玩家，它会选择最大评估值的子节点。
- 对于最小玩家，它会选择最小评估值的子节点。

## 应用场景

- 极小极大搜索通常用于两人对弈游戏，如围棋、象棋、井字棋等。
- 它也可以用于解决某些搜索问题，如拼图游戏、路径规划等。

## 图例

```bash
        root              # 结果      8;
       / |  \
      /  |   \
     /   |    \
    /    |     \
   /     |      \
 min    min     min       # 对方    8,    5     2; 
 / \    / \     / \
max max max max max max   # 下一步 8, 9, 7, 5, 2, 9; 
/ \ / \ / \ / \ / \ / \
5 8 9 x 5 0 7 y 2 1 9  z  # 当前选择
```

## 复杂度

- 时间复杂度：$O(b^d)$
- 空间复杂度：$O(b \cdot d)$

其中，$b$ 是分支因子，$d$ 是树的深度。

### 可选优化

#### alpha-beta pruning 剪枝：减少搜索空间，提高搜索效率

```bash
root
= max(  
    min(max(5,8), max(9, x)),
    min(max(5,0), max(7,y)),
    min(max(2,1), max(9,z))
    )
= max(
    min(8, max(9, x)),
    min(5, max(7,y)),
    min(2, max(9,z))
    )
= max(8, 5, 2)
= 8
```

由于计算量很大, 所以尽量去掉不需要计算的分支.
x, y, z 的取值并不影响结果, 所以图中的x,y,z可以剪掉, 不需要继续遍历计算了

#### 置换表：缓存搜索结果，避免重复搜索