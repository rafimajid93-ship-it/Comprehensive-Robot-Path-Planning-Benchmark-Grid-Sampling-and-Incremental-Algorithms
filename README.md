# Comprehensive Robot Path-Planning Benchmark

A reproducible simulation-based study comparing classical and modern robot path-planning algorithms in static and changing environments.

This project evaluates **grid-based**, **sampling-based**, and **incremental replanning algorithms** under different map structures, obstacle densities, and robot footprints.

## Project Overview

Robot navigation requires efficient path planning methods that can handle different environments and constraints. This project provides a comprehensive benchmark of multiple path-planning approaches using a controlled 2D simulation framework.

The implemented algorithms include:

### Grid-Based Planners

* **Dijkstra's Algorithm**
* **A* Search**
* **Greedy Best-First Search**

### Sampling-Based Planners

* **Rapidly-exploring Random Tree (RRT)**
* **RRT***
* **Probabilistic Roadmap (PRM)**

### Incremental Planner

* **D* Lite**

The study compares their performance in both:

* Static environments
* Dynamically changing environments requiring replanning

---

## Research Questions

This benchmark investigates:

* How do different planners perform under varying obstacle densities?
* How do planning approaches trade off between speed, path quality, and reliability?
* How does robot size influence navigation performance?
* How effective is incremental replanning compared with complete replanning?
* Which algorithm provides the best balance between reliability and efficiency?

---

## Features

✅ Multiple environment generation methods:

* Open maps
* Random obstacle maps
* Maze environments
* Warehouse-like environments
* Narrow passage environments

✅ Robot footprint modeling through obstacle inflation

✅ Collision checking and path validation

✅ Automated correctness testing

✅ Performance evaluation using:

* Success rate
* Runtime
* Path length
* Optimality ratio
* Nodes explored
* Clearance from obstacles

✅ Extensive visualization:

* Path comparison plots
* Algorithm performance graphs
* Heatmaps
* Runtime comparisons
* Parameter sensitivity analysis
* RRT* convergence analysis

---

## Algorithms Compared

| Algorithm  | Category       | Main Advantage                  |
| ---------- | -------------- | ------------------------------- |
| Dijkstra   | Graph Search   | Guarantees optimal path         |
| A*         | Graph Search   | Optimal with heuristic guidance |
| Greedy BFS | Graph Search   | Faster but not always optimal   |
| RRT        | Sampling-Based | Handles complex spaces          |
| RRT*       | Sampling-Based | Improves path optimality        |
| PRM        | Sampling-Based | Good for repeated queries       |
| D* Lite    | Incremental    | Efficient dynamic replanning    |

---

## Experimental Setup

The benchmark evaluates planners under:

* Different obstacle densities
* Different robot radii
* Multiple random seeds
* Various environment structures

Both deterministic and stochastic algorithms are tested using consistent evaluation conditions.

---

## Dynamic Replanning Experiment

The project evaluates **D* Lite** against repeated A* replanning when obstacles change during navigation.

The experiment measures:

* Replanning time
* Search effort
* Path quality after changes

---

## Results

The notebook automatically generates:

* Comparison tables
* CSV result files
* Performance graphs
* Algorithm ranking based on multiple evaluation criteria

Generated outputs include:

```
cse543_results/
│
├── CSV result tables
├── Performance plots
├── Heatmaps
├── Sensitivity analysis graphs
└── Dynamic replanning analysis
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/robot-path-planning-benchmark.git
```

Install required dependencies:

```bash
pip install numpy pandas matplotlib seaborn scipy
```

Run the notebook:

```bash
jupyter notebook
```

---

## Requirements

* Python 3.x
* NumPy
* Pandas
* Matplotlib
* Seaborn
* SciPy
* Jupyter Notebook

---

## How to Use

1. Open the notebook.
2. Configure experiment settings:

```python
QUICK_MODE = True
```

Use Quick Mode for testing.

For complete benchmarking:

```python
QUICK_MODE = False
```

3. Run all cells.
4. Analyze generated tables and visualizations.

---

## Project Structure

```
Robot-Path-Planning-Benchmark/

│
├── Robot_Path_Planning_Benchmark.ipynb
├── README.md
├── requirements.txt
└── cse543_results/
```

---

## Limitations

* This project is a controlled 2D simulation benchmark.
* It does not represent real robot hardware validation.
* Results depend on environment generation and selected parameters.

---

## Future Improvements

Possible extensions:

* 3D navigation environments
* Real robot implementation
* ROS/ROS2 integration
* LiDAR-based mapping
* Reinforcement learning-based planners
* Multi-agent path planning

---

## Author

**Md. Ahanf Tahmid**
**Md. Mahmud Hasan**

Course: CSE543 - Introduction to Robotics
North South University

---

## License

This project is intended for academic and research purposes.
