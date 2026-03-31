# RouteAI
#  RouteAI: AI Logistics Navigation System

A modular AI-driven pathfinding system designed for industrial warehouse optimization. This project simulates a **Goal-Based Rational Agent** that navigates a 10x10 grid to find the most efficient route from a Charging Dock to a Delivery Target.

---

## System Architecture
This project follows a professional **Modular Design Pattern**, separating environment logic from the search engine.

<img width="471" height="115" alt="image" src="https://github.com/user-attachments/assets/75379620-ca00-497e-9649-861194b073c0" />

---

## How the AI "Thinks"
The agent utilizes **Informed Search (A*)** to prioritize paths that mathematically minimize travel distance. It evaluates every move using the function:

**$$f(n) = g(n) + h(n)$$**

* **$g(n)$: The actual cost (steps) taken from the Start to the current position.**
* **$h(n)$: The **Manhattan Distance** heuristic, estimating the remaining distance to the Goal:
  $$|x_{goal} - x_n| + |y_{goal} - y_n|$$**

---

## Getting Started

## 1. Prerequisites
Ensure you have **Python 3.x** installed. No external libraries (like `numpy`) are required as this uses standard Python data structures.

## 2. Running the Simulation
    Making sure all the files are in the same folder
    Navigate to the project directory and run the controller:
    python main_runner.py
    

## 3. Understanding the Output

    S : Start Point (Logistics Dock)

    G : Goal Point (Package Target)

    # : Static Obstacles (Warehouse Shelves)

    * : The Optimal Path calculated by the AI

## Project Observations

    Optimality: The agent consistently finds the shortest path while avoiding all 11+ static obstacles.

    Efficiency: By using a heuristic, the agent reduces the search space significantly compared to uninformed methods like BFS.

    Rationality: The agent demonstrates "perfect rationality" within this discrete, static environment.

Developed by:Kritika Jain
Reg no. : 25BAI10446
Course: Introduction to AI | B.Tech CSE (AI/ML)




