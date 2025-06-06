# Pathfinding Visualizer Documentation
## Project Overview
This project is a React-based web application that visualizes pathfinding algorithms on a grid. It allows users to interactively create obstacles (walls) and then run algorithms like Dijkstra's algorithm, Breadth-First Search (BFS), and Depth-First Search (DFS) to find the shortest path between a start and finish node.
**Key Features:**
*   Interactive grid creation with draggable walls.
*   Visualization of Dijkstra's algorithm.
*   Visualization of Breadth-First Search (BFS) algorithm.
*   Visualization of Depth-First Search (DFS) algorithm.
*   Clear grid functionality.
*   Move start and end nodes.
**Supported Platforms/Requirements:**
*   Modern web browsers (Chrome, Firefox, Safari, Edge).
*   JavaScript enabled.
## Getting Started
1.  **Installation:**
    Clone the repository to your local machine:
    ```bash
    git clone <repository_url>
    ```
    
    Navigate to the project directory:
    ```bash
    cd my-app
    ```
    
    Install the dependencies:
    ```bash
    npm install
    ```
2.  **Running the Application:**
    Start the development server:
    ```bash
    npm start
    ```
    
    This will open the application in your default web browser, usually at `http://localhost:3000`.
    
**Key Components:**
*   **`PathfindingVisualizer.js`:** This component is the heart of the application. It manages the grid state, handles user interactions (mouse clicks, dragging), and orchestrates the visualization of the pathfinding algorithms.  It contains the main logic for running the algorithms and animating the results.
*   **`Node.js`:** This component represents a single node (cell) in the grid. It's responsible for rendering the node's appearance based on its properties (start, finish, wall, visited, shortest path).
*   **`bfs.js`, `dfs.js`, `dijkstra.js`:** These files contain the implementations of the respective pathfinding algorithms. They take the grid, start node, and finish node as input and return the order in which nodes were visited.
## API Documentation
This project does not have a traditional API in the sense of HTTP endpoints. However, the core logic of the pathfinding algorithms can be considered an internal API.
**Algorithms:**
*   **`bfs(grid, startNode, finishNode)`:**
    *   **Input:**
        *   `grid`: A 2D array representing the grid, where each element is a node object.
        *   `startNode`: The starting node object.
        *   `finishNode`: The destination node object.
    *   **Output:** An array of visited nodes in the order they were visited.
    ```javascript
    import { bfs } from './algorithms/bfs';
    const visitedNodesInOrder = bfs(grid, startNode, finishNode);
    ```
    
*   **`dfs(grid, startNode, finishNode)`:**
    *   **Input:**
        *   `grid`: A 2D array representing the grid, where each element is a node object.
        *   `startNode`: The starting node object.
        *   `finishNode`: The destination node object.
    *   **Output:** An array of visited nodes in the order they were visited.
    ```javascript
    import { dfs } from './algorithms/dfs';
    const visitedNodesInOrder = dfs(grid, startNode, finishNode);
    ```
    
*   **`dijkstra(grid, startNode, finishNode)`:**
    *   **Input:**
        *   `grid`: A 2D array representing the grid, where each element is a node object.
        *   `startNode`: The starting node object.
        *   `finishNode`: The destination node object.
    *   **Output:** An array of visited nodes in the order they were visited.
    ```javascript
    import { dijkstra } from './algorithms/dijkstra';
    const visitedNodesInOrder = dijkstra(grid, startNode, finishNode);
    ```
    
*   **`getNodesInShortestPathOrderBFS(finishNode)`:**
    *   **Input:**
        *   `finishNode`: The destination node object.
    *   **Output:** An array of nodes in the shortest path order.
    ```javascript
     import { getNodesInShortestPathOrderBFS } from './algorithms/bfs';
    const nodesInShortestPathOrder = getNodesInShortestPathOrderBFS(finishNode);
    ```
    
*   **`getNodesInShortestPathOrderDFS(finishNode,startNode)`:**
    *   **Input:**
        *   `finishNode`: The destination node object.
        *   `startNode`: The starting node object.
    *   **Output:** An array of nodes in the shortest path order.
    ```javascript
     import { getNodesInShortestPathOrderDFS } from './algorithms/dfs';
    const nodesInShortestPathOrder = getNodesInShortestPathOrderDFS(finishNode,startNode);
    ```
    
*   **`getNodesInShortestPathOrderDijkshtra(finishNode)`:**
    *   **Input:**
        *   `finishNode`: The destination node object.
    *   **Output:** An array of nodes in the shortest path order.
    ```javascript
     import { getNodesInShortestPathOrderDijkshtra } from './algorithms/dijkstra';
    const nodesInShortestPathOrder = getNodesInShortestPathOrderDijkshtra(finishNode);
    ```
