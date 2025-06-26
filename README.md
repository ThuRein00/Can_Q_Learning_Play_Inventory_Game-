# Inventory Optimization using Q-learning

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://python.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow)](https://opensource.org/licenses/MIT)

This project applies Q-learning; a popular reinforcement learning to optimize inventory management decisions under stochastic demand conditions. It benchmarks RL performance against a globally optimal (s,S) policy.

## 📌 Project Overview

### Question
"How well can Q-learning solve inventory management problems in stochastic environments?"

### Key Components
- **Inventory simulation environment** with stochastic demand
- **Q-learning agent** implementation
- **Global optimal policy search** for benchmarking
- **Performance evaluation** 

### Problem Formulation
**States**: On-hand inventory at end of day (0-30 vehicles)  
**Actions**: Order quantity (0-30 vehicles)  
**Reward**: -(Holding Cost + Ordering Cost + Shortage Cost)  
**Objective**: Minimize total costs over 100-day horizon

## 📊 Key Results
| Metric | Global Optimal | Q-learning |
|--------|----------------|------------|
| **Mean Total Cost** | $95,292 | $97,203 |
| **Shortage Probability** | 6.4% | 9.6% |
| **Performance** | 100% | 98% |

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Required packages:
```bash
pip install simpy numpy matplotlib seaborn
```

### Project Structure
```bash
inventory-rl/
├── data/                   # Simulation output data
├── docs/                   # Presentation slides
├── src/
│   ├── global_optimal_search.py   # Finds optimal (s,S) policy
│   ├── main.py                    # Trains & evaluates Q-agent
│   ├── Q_learning_agent.py        # Q-learning implementation
│   └── simulation_model.py        # Inventory environment
└── README.md
```

### Running the Project

### Find global optimal policy:
```bash
python src/global_optimal_search.py
```

### Train and evaluate Q-learning agent:
```bash
python src/main.py
```



