# Resource Allocation Graph (RAG) Visualizer 🔄

[![Live Demo](https://img.shields.io/badge/Live-Demo-brightgreen.svg)](https://nikhilesh-0.github.io/os-deadlock-visualizer/)
[![Tech Stack](https://img.shields.io/badge/Tech-HTML%20%7C%20CSS%20%7C%20Vanilla%20JS-blue)](#)
[![Concept](https://img.shields.io/badge/OS-Deadlock%20Detection-purple)](#)

An interactive, client-side web application built to simulate and detect deadlocks in Operating Systems using Resource Allocation Graphs (RAG). 

This tool allows users to dynamically build complex graphs of Processes and Resources, utilizing a Depth-First Search (DFS) algorithm to actively monitor for circular waits and evaluate system states in real-time.

## 🚀 Live Demo
**[Try the interactive visualizer here!](https://nikhilesh-0.github.io/os-deadlock-visualizer/)**

## ✨ Key Features

* **Interactive Graph Engine:** Click-and-drop interface to add Process nodes (blue circles) and Resource nodes (green squares) to a grid canvas.
* **Dynamic Edge Routing:** Draw directional arrows to represent "Request" (Process → Resource) and "Assignment" (Resource → Process) edges.
* **Real-time Deadlock Detection:** Implements a DFS-based cycle detection algorithm (`O(V + E)` complexity) that continuously monitors the graph.
* **Visual Warnings:** Instantly highlights cycles in red and alerts the user when a deadlock occurs.
* **Educational Presets:** One-click loading of predefined scenarios, including Safe States, 2-Process Deadlocks, and 3-Process Deadlocks.
* **OS Theory Integration:** Built-in reference panel detailing Coffman's 4 Conditions for deadlock (Mutual Exclusion, Hold & Wait, No Preemption, Circular Wait).

## 🛠️ Tech Stack

This project was built intentionally without external frontend frameworks or heavy libraries to ensure maximum performance and core language mastery:
* **HTML5:** Semantic structure and UI layout.
* **CSS3:** Custom styling, CSS grid/flexbox, and CSS variables for a modern dark-mode theme.
* **Vanilla JavaScript (ES6+):** Canvas rendering (`CanvasRenderingContext2D`), state management, graph data structures, and the DFS traversal algorithm.

## 🧠 How the Algorithm Works

The application represents the current state of processes and resources as a directed graph. 
1. Every time a node or edge is added/removed, an adjacency list is rebuilt.
2. A Depth-First Search (DFS) algorithm traverses the graph, keeping track of visited nodes and the current recursion stack.
3. If the algorithm encounters a node that is already in the current recursion path, a **cycle** is identified.
4. Because this is a single-instance resource model, the presence of a cycle directly proves **Circular Wait**, mathematically confirming a deadlock state.

## 💻 Local Execution

Since this is a fully static client-side application, running it locally requires zero setup.

1. Clone the repository:
   ```bash
   git clone [https://github.com/nikhilesh-0/os-deadlock-visualizer.git](https://github.com/nikhilesh-0/os-deadlock-visualizer.git)