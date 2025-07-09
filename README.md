# Optimization Technique Meal Planning

This project aims to generate optimal meal plans that balance cost and nutritional value, or both, using optimisation techniques. The generated meal plans will be both cost-effective and nutritionally balanced, leveraging both single-objective and multi-objective optimization strategies.

## What It Does

The notebooks in this repository formulate the meal planning problem as an optimization task with the following objectives:
**Single Objective Optimization:** Single Objective Optimization (SOO) aims to **optimize one goal** — either minimizing or maximizing a single objective function — while satisfying various constraints.

**Example:**
  Objective: Minimize total meal cost  
  Constraints:  
  - Calories ≥ 2000  
  - Protein ≥ 50g  
  - Fat ≤ 70g  
  - Sugar ≤ 30g.
  ✅ Best used when only one goal matters (e.g., lowest cost). 


**Multi-Objective Optimization:** Multi-Objective Optimization (MOO) handles **two or more conflicting objectives** that must be optimized simultaneously.

**Example:**
Objectives:  
1. Minimize total cost  
2. Maximize total protein

Constraints:  
  - Calories ≥ 2000  
  - Sugar ≤ 30g  
  - Sodium ≤ 2300mg

MOO doesn't return a single solution — instead, it generates a Pareto front, offering a set of trade-off solutions where no one solution is best in all aspects.

✅ Use when decisions involve trade-offs (e.g., cost vs. nutrition quality).


The project implements and compares several optimization algorithms, analyzes their solutions, and discusses their strengths and weaknesses in the context of meal planning.

## Features
- Optimize meals based on nutritional data (cost, calories, protein, fat, etc.)
- Support for constraint-based planning (e.g., minimum protein intake)
- Output best or balanced meals using optimization algorithms
- Multi-objective support using Pareto front (NSGA-II) or weighted sum
- Visualization of cost-nutrition trade-offs

## Approaches Used

### 1. Linear Programming (Single Objective)
- **Goal:** Minimize the total cost of the meal plan.
- **Method:** Linear programming is used to select the optimal combination of foods to satisfy nutritional requirements at the lowest possible cost.
- **Characteristics:** Fast, efficient, provides an exact solution.

### 2. Genetic Algorithm (GA) for Single Objective
- **Goal:** Minimize the total cost.
- **Method:** A genetic algorithm simulates natural selection to evolve a population of meal plans towards lower cost, subject to nutritional constraints.
- **Characteristics:** Flexible, can handle non-linear constraints, suitable for more complex or non-convex problems.

### 3. Weight Sum Method with Genetic Algorithm (Multi-Objective)
- **Goal:** Minimize cost and maximize nutrients by combining objectives into a single weighted sum.
- **Method:** The two objectives are combined into one by assigning user-defined weights, and a genetic algorithm is used to optimize this aggregate objective.
- **Characteristics:** Allows flexible trade-offs between objectives, but the outcome depends on the choice of weights.

### 4. NSGA-II (Non-dominated Sorting Genetic Algorithm II) (Multi-Objective)
- **Goal:** Simultaneously minimize cost and maximize nutrients, producing a set of Pareto-optimal solutions.
- **Method:** NSGA-II is a state-of-the-art multi-objective evolutionary algorithm that finds a diverse set of trade-off solutions (Pareto front) without requiring weight selection.
- **Characteristics:** Provides a range of optimal solutions showing different trade-offs, well-suited for problems with conflicting objectives.

## Comparison of Approaches

| Approach                                       | Problem Type         | Solution Quality  | Computational Time | Flexibility | Outcome Highlights                                 |
|------------------------------------------------|---------------------|-------------------|-------------------|-------------|----------------------------------------------------|
| Linear Programming (LP)                        | Single Objective    | High (exact)      | Fast              | Limited     | Finds the lowest-cost meal plan meeting constraints |
| Genetic Algorithm (GA) - Single Objective      | Single Objective    | Good              | Moderate          | High        | Handles complex/nonlinear constraints               |
| Weight Sum Method with GA - Multi-Objective    | Multi-Objective     | Good              | Moderate          | High        | Balances cost and nutrients, sensitive to weights   |
| NSGA-II (Multi-Objective Genetic Algorithm)    | Multi-Objective     | Pareto-optimal    | Higher            | Very High   | Offers diverse trade-offs, best for real-world use  |

### Which One Has Better Outcome?

- **Single Objective:**  
  - **Linear Programming** is the best for simple cost minimization with linear constraints, offering guaranteed optimal solutions quickly.
  - **Genetic Algorithm** is preferable if the problem has non-linear or more complex constraints.
- **Multi-Objective:**  
  - **NSGA-II** provides the best overall outcome, delivering a set of Pareto-optimal meal plans that allow the user to choose a preferred trade-off between cost and nutrients.
  - **Weight Sum Method** is useful for generating a single solution based on user preferences, but is sensitive to how weights are assigned.

## How to Use

1. **Clone the repository:**
   ```bash
   git clone https://github.com/JamiyaAlom/optimization-technique-meal-planning.git
   ```
2. **Open the notebooks:**  
   Use Jupyter Notebook, JupyterLab, or VS Code to explore each optimization approach.
3. **Experiment:**  
   Add your datasets, Adjust nutritional constraints, cost weights, and optimization parameters as needed.
4. **Analyze Results:**  
   Visualizations and summary statistics are provided in each notebook for comparison.

## Dependencies

- Python 3.x
- Jupyter Notebook
- numpy
- pandas
- scipy
- matplotlib
- PuLP (for linear programming)
- [Other libraries as specified in the notebooks]

## Results

Each notebook presents:
- The optimal meal plans for the given objectives and constraints.
- Comparative analysis of cost, nutritional value, and trade-offs.
- Visualizations of the Pareto front (for multi-objective optimization).
- Discussion of practical implications and recommendations.

---

Feel free to explore, modify, and extend the approaches for your own meal planning or other optimization problems!