CIS 700 course project

This project presents a full-stack motion planning and control framework for robotic block stacking using a simulated 6-DOF robotic arm (Poppy Ergo Jr) in PyBullet. It combines analytical and numerical inverse kinematics, trajectory control, and a tower rearrangement planner optimized with A* search.

## Project Objectives

- Simulate a 6-DOF robotic arm using PyBullet
- Implement inverse and forward kinematics
- Design a rule-based tower rearrangement planner
- Perform collision-free motion planning with optimized A*
- Evaluate block stacking accuracy and reliability
- Experiment with RRT* for trajectory exploration

## Features

- Inverse Kinematics with L-BFGS-B optimization
- Rule-based tower rearrangement with auxiliary storage
- A* and RRT* path planning algorithms
- Real-time joint-space control and grasping
- Detailed visualization using PyBullet and OpenCV
- Tower abstraction and block placement optimization

## How It Works
- IK Solver: Uses L-BFGS-B to compute joint angles that match a target 6D pose.
- Tower Planner: Encodes scene state into stacks; determines which block to move and where.
- Move Optimization: A* minimizes redundant transfers.
- Simulation: Executes motion with joint-space interpolation and grasp logic.

## Project Structure

| File | Description |
|------|-------------|
| `A_star.py`, `A_star_optimized.py` | Greedy and optimized A* planners |
| `rrt_star.py` | Experimental implementation of RRT* |
| `evaluation.py` | Performance metrics for stacking success |
| `example.py` | Sample simulation runner |
| `simulation.py` | Main simulation coordinator |
| `poppy_ergo_jr.pybullet.urdf` | 6-DOF robot arm model for PyBullet |
| `semester_projects.pdf` | Project documentation/report |

## 🖥Requirements

- Python 3.7+
- PyBullet
- NumPy
- SciPy
- OpenCV
- Matplotlib
- PyTorch

## Install dependencies:

```bash
pip install pybullet numpy scipy opencv-python matplotlib torch
```

## Current results
- Success rate: 60% over 30 randomized trials
- Average planning time: 1.8 seconds
- Mean position error: ~0.019 m
- Rotation error: ~11°

