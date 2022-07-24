---
title: DFS and BFS
tags:
 - Algorithm
 - Graph Algorithm
---

Depth-first search (DFS) and breadth-first search (BFS) are both algorithms used for traversing or searching graphs.

<!--more-->

## Depth-First Search

A DFS algorithm will start at an arbitrary node in a graph, and then explores as far as possible. When there are no more nodes left to explore,
the algorithm backtracks to the previous node explored.

### Example

![dfs ex][graph]

Lets do a depth-first search on the graph above starting at node A, assuming that nodes on the left are searched before the nodes on the right.

* First, we'll go to node B, then E. Since there is nowhere else to go from E, we come back to B.
* Then, we'll go to F to G, and come back to B because G is a dead end, and there is nowhere else to go from F.
* Now, we have been to all neighbouring nodes of B, so we come back to A, and move on to C.
* From C, we'll move to D, and since we've already been to A, we'll go to H.
* H is a dead end, there is nowhere to go from D and C, so we return back at A.
* There are no more nodes left unvisited that can be reached from A, thus we are done.

In conclusion, we traverse the nodes in the following order: A B E F G C D H

Similarly, if we started from B, the order of traversal woulde be: B E F G A C D H (assuming that nodes on the bottom are searched before nodes on the top)

### Code Example

The following is an implementation of DFS in C++.

```cpp
vector<int> traversal,graph[V+1];
bool visited[V+1];

void dfs(int u){
  visited[u] = true;
  traversal.push_back(u);
  for(int i = 0; i < graph[u].size(); i++){
    int next = graph[u][i];
    if(visited[next] == false)
      dfs(next);
  }
}
```

Variable explanation:

* graph: The adjacency list of the graph
* visited: A boolean array that keeps track of nodes that have been previously visited
* traversal: A vector that stores the nodes in the order they were traversed
* u: The node that is currently being searched
* next: The node that is going to be searched next

Code explanation:

First, node u is marked as visited using the visited array. Then node u is pushed into the traversal vector.
Within the for loop, the if statement checks if each of the adjacent nodes of node u have been visited. If the next node hasn't been visited,
we continue searching from the next node using recursion.


[graph]: https://raw.githubusercontent.com/Equinox134/equinox134.github.io/master/assets/images/logo/2022-07-24-dfs-and-bfs/graph.png
