# 🚚 Supply Chain Optimization using Linear Programming (PuLP)

## 📌 Overview

This project models a **supply chain transportation problem** using Linear Programming in Python.
The goal is to determine the most cost-efficient way to transport goods from multiple warehouses to retail stores while satisfying supply and demand constraints.

---

## 🎯 Objective

Minimize total transportation cost while:

* Meeting demand at each store
* Not exceeding warehouse supply limits

---

## 🧠 Problem Description

We consider:

* **2 Warehouses** with limited supply
* **3 Stores** with fixed demand
* **Different shipping costs** between each warehouse and store

The model decides how many units to ship along each route.

---

## 📊 Data

### Warehouses (Supply)

| Warehouse | Capacity |
| --------- | -------- |
| W1        | 100      |
| W2        | 150      |

### Stores (Demand)

| Store | Demand |
| ----- | ------ |
| S1    | 80     |
| S2    | 120    |
| S3    | 50     |

### Shipping Costs (per unit)

| From → To | S1 | S2 | S3 |
| --------- | -- | -- | -- |
| W1        | 2  | 4  | 5  |
| W2        | 3  | 1  | 7  |

---

## ⚙️ Approach

The problem is formulated as a **Linear Programming (LP) model**:

* **Decision Variables**
  Amount shipped from warehouse *w* to store *s*

* **Objective Function**
  Minimize total transportation cost

* **Constraints**

  * Supply constraints (warehouse capacity)
  * Demand constraints (store requirements)

---

## 🧑‍💻 Implementation

* Language: Python
* Library: PuLP

### Key Steps:

1. Define decision variables
2. Set up objective function
3. Add supply and demand constraints
4. Solve using PuLP solver
5. Analyze results

---

## ✅ Results

Optimal solution:

* W1 → S1 = 50
* W1 → S3 = 50
* W2 → S1 = 30
* W2 → S2 = 120

**Total Minimum Cost = 560**

---

## 🔍 Insights

* Cheapest routes are prioritized (e.g., W2 → S2)
* Expensive routes are avoided when possible
* All supply and demand constraints are exactly satisfied

---

## 🚀 Extensions

The model can be extended with:

* Route restrictions
* Penalties for unmet demand
* Fixed warehouse operating costs
* Multiple time periods

---

## 📁 How to Run

1. Install dependencies:

```bash
pip install pulp
```

2. Run the Python script or Jupyter Notebook

---

## 📌 Key Learnings

* Formulating real-world problems as LP models
* Understanding constraints and feasibility
* Interpreting optimal solutions
* Sensitivity to constraint changes

---

## 📎 Future Work

* Visualization of transportation network
* Integration with real-world datasets
* Use of advanced solvers (e.g., Gurobi, CPLEX)

---
