 Dynamic Pathfinding Agent

A grid-based pathfinding visualiser built with Python and Tkinter that demonstrates **A* Search** and **Greedy Best-First Search (GBFS)** with real-time dynamic obstacle spawning and automatic re-planning.


 1. Overview

The Dynamic Pathfinding Agent is an interactive educational tool designed to demonstrate and compare informed search algorithms in both static and dynamic grid environments.

The system allows users to:

* Generate random obstacle maps
* Manually edit grid layouts
* Select algorithms and heuristics
* Observe real-time search expansion
* Enable dynamic obstacle spawning
* Monitor performance metrics

The project clearly separates algorithmic logic from graphical components, ensuring modularity and maintainability.
2. Features

Two Search Algorithms

  * A* Search
  * Greedy Best-First Search

Three Heuristics (Selectable at Runtime)

  * Manhattan Distance
  * Euclidean Distance
  * Chebyshev Distance

* Animated Visualisation

  * Yellow frontier nodes
  * Blue expanded nodes
  * Green final path
  * Red dynamic obstacles

* Dynamic Mode

  * Obstacles spawn randomly during execution
  * Automatic path re-planning

* Interactive Map Editor

  * Place or erase walls
  * Move Start and Goal nodes

* Random Map Generator

  * Custom grid size
  * Adjustable obstacle density

* Real-Time Metrics

  * Nodes visited
  * Path cost
  * Execution time
  * Re-plan count

* Full Animation Controls

  * Run
  * Pause
  * Resume
  * Stop

3. Project Structure

```
dynamic-pathfinding-agent/
├── code.py
├── visuals.py
└── README.md
```

code.py

Contains:

* A* implementation
* GBFS implementation
* Heuristic functions
* Grid utilities
* Dynamic obstacle logic
* Performance tracking

No GUI dependencies.

visuals.py

Contains:

* Tkinter interface
* Animation engine
* User controls
* Metrics dashboard

---
4. Requirements

* Python 3.8 or higher
* Tkinter (included with Python on Windows and macOS)

Check Python Version

```
python --version
```

---
 5. Installation

Step 1 — Clone Repository

```bash
git clone https://github.com/your-username/dynamic-pathfinding-agent.git
cd dynamic-pathfinding-agent
```

Step 2 — Install Tkinter (If Required)

Windows
Tkinter is included with official Python installer.

macOS

```bash
brew install python-tk
```

Ubuntu / Debian

```
sudo apt-get update
sudo apt-get install python3-tk
```

Fedora / RHEL

```
sudo dnf install python3-tkinter
```

Step 3 — Verify Installation

```
python -c "import tkinter; print('Tkinter OK:', tkinter.TkVersion)"
```

---
6. How to Run

Ensure both files are in the same directory.

```bash
python visuals.py
```

The GUI window will open.

---
 7. Using the Application

7.1 Generate a Grid

1. Set number of rows and columns
2. Set obstacle density percentage
3. Click **Generate Random Map**

Alternatively, click Clear Grid to create a blank grid.

---
 7.2 Edit the Map

Select an editing mode and click or drag on the grid.

| Mode  | Action           |
| ----- | ---------------- |
| Wall  | Place obstacles  |
| Erase | Remove obstacles |
| Start | Move start node  |
| Goal  | Move goal node   |

---

7.3 Choose Algorithm and Heuristic

Select before running:

Algorithms

* A* Search → f(n) = g(n) + h(n)
* Greedy Best-First Search → f(n) = h(n)

**Heuristics**

* Manhattan → |dr| + |dc|
* Euclidean → sqrt(dr² + dc²)
* Chebyshev → max(|dr|, |dc|)

---

 7.4 Enable Dynamic Mode (Optional)

When enabled:

* Obstacles spawn randomly during movement
* The agent re-plans if its path becomes blocked

---

7.5 Run Search

Click Run Search

Execution phases:

1. Node expansion visualisation
2. Final path display
3. Agent movement animation

---

7.6 Controls

| Button         | Function          |
| -------------- | ----------------- |
| Run Search     | Start execution   |
| Pause / Resume | Control animation |
| Stop           | Cancel execution  |
| Clear Grid     | Reset grid        |

---

=8. Metrics Dashboard

After completion, the following metrics are displayed:

| Metric         | Description                 |
| -------------- | --------------------------- |
| Nodes Visited  | Total expanded nodes        |
| Path Cost      | Steps in final path         |
| Execution Time | Total computation time (ms) |
| Re-plan Count  | Number of dynamic re-plans  |

---

9. Colour Legend

| Colour       | Meaning            |
| ------------ | ------------------ |
| Green (S)    | Start node         |
| Amber (G)    | Goal node          |
| Yellow       | Frontier           |
| Blue         | Expanded nodes     |
| Green path   | Final path         |
| Red (A)      | Agent              |
| Dark grey    | Wall               |
| Flashing red | Newly spawned wall |

---

10. Algorithm Details

10.1 A* Search

Uses:

f(n) = g(n) + h(n)

* g(n) = exact cost from start
* h(n) = heuristic estimate

Guarantees optimal path if heuristic is admissible and consistent.

---

10.2 Greedy Best-First Search

Uses:

f(n) = h(n)

* Ignores accumulated path cost
* Faster in simple grids
* Does not guarantee optimal solution

---

11. Conclusion

The Dynamic Pathfinding Agent provides a comprehensive platform to study informed search algorithms under both static and dynamic conditions.

Through real-time visualisation, heuristic selection, and performance metrics, users can clearly observe:

* The optimality of A*
* The speed trade-off of GBFS
* The impact of heuristic quality
* The computational cost of dynamic re-planning

The modular design ensures extensibility and makes the project suitable for academic demonstrations, experimentation, and further research in intelligent pathfinding systems.
