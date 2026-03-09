# Toll-Modelization-MMs: Toll Plaza Queueing Simulation

![Author](https://img.shields.io/badge/Author-Your%20Name-blue)
![Python](https://img.shields.io/badge/Python-3.8+-blue)
![NumPy](https://img.shields.io/badge/NumPy-Supported-013243)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Supported-11557c)

A Python simulation of a highway toll plaza using a **Multi-Server Markovian System (M/M/s queue)**.  
It models vehicle arrivals and service times across different payment types (**telepayment, card, cash**) to analyze queue dynamics and optimize booth allocation.

---

# 📁 Project Structure

```bash
Toll-Modelization-MMs/
├── src/
│   └── main.py
├── requirements.txt
└── README.md
```

## 🛠️ Scripts Description

### `src/main.py`

The core orchestration script for the queuing simulation. It handles user inputs, sets up the toll plaza environment, and executes the time-step simulation.

#### Statistical Modeling
Implements a **Poisson arrival process** (arrival rate $\lambda$) and **exponential service times** (service rate $\mu$).

#### Dynamic Routing
Manages the state of the toll plaza at each time increment, routing incoming vehicles to the optimal payment booths (**Telepayment, Credit Card, or Cash**) based on real-time queue lengths.

#### Visualization
Generates dynamic **Matplotlib plots** to:
- Visualize queue states at specific time intervals
- Track the average vehicle flow per booth during the simulation

---

## 🎯 Objective

The objective of this project is to **model and simulate traffic flow at a toll plaza using queuing theory**.

By approximating **continuous Markov processes in discrete time**, the simulation provides a sandbox environment to analyze how adjusting the number of specific payment booths affects:

- Waiting times  
- Queue lengths  
- Overall system efficiency  

---

## ⚠️ Notes

- The simulation builds random variables using custom implementations of **Cumulative Distribution Functions (CDFs)** based on the **negative exponential distribution**.

- The script currently runs a **discrete-time approximation**.  
  Using extreme parameter values (**very high $\lambda$ or very low $\mu$**) may require adjusting the **time step definition** to maintain simulation accuracy.
