# Meal Planning Optimisation Project

This project aims to generate optimal meal plans that balance cost and nutritional value, or both, using optimisation techniques. It includes:

- **Single-objective optimization**: minimising cost.
- **Multi-objective optimization**: balancing cost (minimising cost) and nutrition (e.g., maximizing protein).

---

## Features

- Optimize meals based on nutritional data (cost, calories, protein, fat, etc.)
- Support for constraint-based planning (e.g., minimum protein intake)
- Output best or balanced meals using optimization algorithms
- Multi-objective support using Pareto front (NSGA-II) or weighted sum
- Visualization of cost-nutrition trade-offs

---

## Optimization Methods

### Single-Objective Optimization
- **Objective**: Optimize for cost 
- **Approaches**:
  - Linear Programming (LP)
  - Genetic Algorithm

**Example Goal**:  
Minimize total cost while meeting nutritional requirements

**Example Output**:
Best Cost: 155.00 Baht
**Meal Plan**:
Selected Food Items Examples:
  Tuna Sandwich | Cost: 30 Baht | Cal: 340.0 | Prot: 36.2 | Fat: 10.4 | Sugar: 2.0 | Sodium: 300.0
  and so on ............. 


## Multi-Objective Optimization
**Objective**: Balance between two or more objectives (e.g., cost vs protein)
- **Approaches**:
  - Weight Sum Methods
  - NSGA-II


