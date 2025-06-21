# Meal Planning Optimisation Project

This project aims to generate optimal meal plans that balance cost and nutritional value, or both, using optimisation techniques. It includes:

- **Single-objective optimization** :minimising cost.
- **Multi-objective optimization** :balancing cost (minimising cost) and nutrition (e.g., maximizing protein).

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
_Minimize total cost while meeting nutritional requirements

**Example Output**:
Best Cost: 155.00 Baht
**Meal Plan**:
Selected Food Items:
  Tuna Sandwich | Cost: 30 Baht | Cal: 340.0 | Prot: 36.2 | Fat: 10.4 | Sugar: 2.0 | Sodium: 300.0
  Ezygo Stir-Fried Pork and Basil with Rice | Cost: 35 Baht | Cal: 460.0 | Prot: 17.0 | Fat: 12.0 | Sugar: 2.0 | Sodium: 690.0
  Ezygo Stir Fried Chicken and
Basil with rice | Cost: 35 Baht | Cal: 430.0 | Prot: 20.0 | Fat: 5.0 | Sugar: 5.0 | Sodium: 680.0
  Natural  Yogurt | Cost: 20 Baht | Cal: 84.0 | Prot: 14.0 | Fat: 0.0 | Sugar: 4.0 | Sodium: 60.0
  Lotus Stick Biscuit: Original Flavor | Cost: 20 Baht | Cal: 560.0 | Prot: 8.0 | Fat: 28.0 | Sugar: 20.0 | Sodium: 190.0
  Taro Spicy Flavoured Fish Snack | Cost: 5 Baht | Cal: 80.0 | Prot: 6.0 | Fat: 0.0 | Sugar: 3.0 | Sodium: 530.0
  Banana | Cost: 10 Baht | Cal: 88.0 | Prot: 1.1 | Fat: 0.3 | Sugar: 12.0 | Sodium: 1.0

**Summary of Best Meal Plan**:
Total Selected Food Items: 7
Total Cost: 155.00 Baht
Total Cal: 2042.0 Kcal. ---- Calory Requirements: Satisfied :)
Total Protein: 102.3 g. ---- Protein Requirements: Satisfied :)
Total fat: 55.699999999999996 g. --------- Fat Requirements: Satisfied :)
Total sugar: 48.0 g. ------- Sugar Requirements: Satisfied :)
Total sodium: 2451.0 mg. --- Sodium Requirements: Satisfied :)
Computation Time: 0.08 



