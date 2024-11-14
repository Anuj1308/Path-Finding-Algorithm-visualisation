# Pathfinding Algorithm Visualization
This repository provides a visualization tool for exploring and understanding four essential pathfinding algorithms: A*, Dijkstra's Algorithm, Breadth-First Search (BFS), and Depth-First Search (DFS). The visualizations are implemented using Python and Pygame, allowing users to experiment with these algorithms on a grid where they can set start and end points and place obstacles.

## Features
Interactive grid: Click to set start, end, and obstacles.
Algorithm selection: Run any of the four pathfinding algorithms to visualize the pathfinding process.
Obstacle mode: Easily toggle obstacle placement mode.
Reset: Clear the grid and try different setups.
## Algorithms
### 1. A* (A-Star) Algorithm
The A* algorithm is a heuristic search algorithm that combines the benefits of Dijkstra's algorithm and greedy best-first search. It uses a heuristic function to guide the search, often leading to the shortest path.<br>
    i. Heuristic: Uses the Manhattan distance for estimating the cost.<br>
    ii. Optimality: Guarantees the shortest path.
    iii. Best suited for: Cases where you want an efficient and accurate shortest path.
### 2. Dijkstra's Algorithm
Dijkstra's algorithm is a graph search algorithm that finds the shortest path from the starting node to all other nodes. It does not use heuristics, making it a pure shortest-path algorithm.
    i. Heuristic: None (guarantees shortest path by evaluating all possible paths).
    ii. Optimality: Guarantees the shortest path.
    iii. Best suited for: Applications requiring the shortest path to every node, not just a specific endpoint.
### 3. Breadth-First Search (BFS)
BFS is a simple, uninformed search algorithm that expands nodes layer by layer, exploring all neighbors of a node before moving on to the next layer. It guarantees the shortest path in an unweighted grid but is not optimal for weighted graphs.
    i. Heuristic: None.
    ii. Optimality: Guarantees the shortest path in unweighted graphs.
    iii. Best suited for: Unweighted grids where you need the shortest path.
### 4. Depth-First Search (DFS)
DFS is a basic graph traversal algorithm that explores as far down one branch as possible before backtracking. It does not guarantee the shortest path.
    i. Heuristic: None.
    ii. Optimality: Does not guarantee the shortest path.
    iii. Best suited for: Situations requiring a path (not necessarily the shortest) or for exploring connected components.

## Differences Between the Algorithms

| Algorithm       | Shortest Path Guarantee       | Optimality  | Best for Weighted Graphs    | Time Complexity           |
|-----------------|-------------------------------|-------------|-----------------------------|----------------------------|
| **A\***         | Yes                           | Optimal     | Yes                         | \(O(E) + O(H(n))\)         |
| **Dijkstra's**  | Yes                           | Optimal     | Yes                         | \(O(V^2)\) or \(O(E + V \log V)\) with priority queue |
| **BFS**         | Yes (Unweighted only)         | Optimal     | No                          | \(O(V + E)\)               |
| **DFS**         | No                            | Not optimal | No                          | \(O(V + E)\)               |

- **A\*** and **Dijkstra's Algorithm** are best suited for weighted graphs where the cost of each edge differs.
- **BFS** is ideal for unweighted graphs or grids, where each step has the same "cost."
- **DFS** is effective for exploring reachable nodes from the start but is not recommended if finding the shortest path is required.

## Choosing the Best Algorithm
### 1. Shortest Path: 
Both A* and Dijkstra's guarantee the shortest path. A* is generally faster due to its heuristic approach.
### 2. Unweighted Graphs: 
BFS is optimal in unweighted grids, as it guarantees the shortest path and is faster in such cases than A* or Dijkstra's.
### 3. Exploration:
DFS is useful for exploring all reachable nodes from the start but is not recommended if the shortest path is required.

## Follow the instructions on the screen:

1. Left-click to place the start, end, and obstacles.
2. Press SPACE to run the algorithm.
3. Press C to clear the grid.
4. Press O to toggle obstacle mode.

## Install **Pygame** if not already installed:

```bash
pip install pygame
