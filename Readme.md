# A* 寻路算法 / A* pathfinding algorithm


用一维数组表示二维平面图, 一个节点最多有8个方向, 没有边;  
节点中保存一个权重, 越高表示通过的开销越大, 小于 0 表示不可通过;

A two-dimensional plan is represented by a one-dimensional array.   
A node has up to eight directions and no edges.  
A weight is stored in the node, the higher the cost of passing,  
the less than ZERO is not passable;


用浏览器打开 index.html

Open index.html with a browser


## DEMO

```js
let fp = new AStarFindPath(10, 10);

// Block the Road
fp.setWeights(8, 9, -1);

// From (0, 0) to (10, 10)
let node = fp.find(0, 0, 10, 10);

// Reverse looking for the parent node
while (node) {
  node = node.from;
}
```