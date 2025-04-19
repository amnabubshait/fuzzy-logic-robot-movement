# 🤖 Fuzzy Logic Control for Robot Speed Based on Obstacle Distance

This project implements a fuzzy logic controller using Python and `scikit-fuzzy` to determine a robot's movement speed based on the distance to an obstacle. The system simulates how a robot should slow down or stop as it approaches an object, mimicking human-like reasoning under uncertainty.

---

## 📌 Assignment Objective

The goal is to understand and implement a fuzzy logic system to solve a real-world control problem using:

- Fuzzy sets and membership functions
- Fuzzy rules
- A fuzzy inference engine
- Defuzzification to produce actionable outputs

---

## 🧠 Problem Statement

In uncertain environments, robots need to make decisions based on incomplete or imprecise information. This system models a robot that adjusts its speed based on how far it is from an obstacle:

- **Close obstacle → Stop**
- **Medium distance → Slow down**
- **Far distance → Move fast**

---

## ⚙️ Fuzzy Logic System Design

### 🔹 Input Variable
- **Distance (cm)**: `0 to 100`
  - Fuzzy sets: `Close`, `Medium`, `Far`

### 🔹 Output Variable
- **Speed (0 to 10 units)**:
  - Fuzzy sets: `Stop`, `Slow`, `Fast`

### 🔹 Fuzzy Rules

1. If distance is **close**, then speed is **stop**
2. If distance is **medium**, then speed is **slow**
3. If distance is **far**, then speed is **fast**
4. If distance is **close AND medium**, then speed is **stop**
5. If distance is **medium AND far**, then speed is **slow**

---

## 🖥️ Implementation

- Language: Python 3.x
- Library: `scikit-fuzzy`
- Visualization: `matplotlib`

### Setup Instructions

```bash
pip install scikit-fuzzy matplotlib numpy
```

### Run the Code

1. Open the Jupyter notebook and execute the cells sequentially.
2. _Fuzzy Sets and Membership Functions:_ Define input and output fuzzy sets and their corresponding membership functions.
3. _Fuzzy Rules and Inference:_ Design fuzzy rules and implement the inference engine.
4. _Testing:_ Test the system with sample input values (e.g., distances) and visualize the results.
5. _Visualizations:_ View graphs of membership functions and output results.

The script:
- Defines fuzzy sets and membership functions
- Creates fuzzy rules
- Runs the fuzzy inference system
- Tests with various distances
- Outputs results and plots

---

## 📊 Sample Output

```
Distance (cm) → Speed (0–10)
-----------------------------
10            →   0.75
30            →   2.42
50            →   4.84
70            →   7.25
90            →   9.12
```

---

## 📈 Visualizations

- Membership functions for `distance` and `speed`
- Inferred output graphs for each input scenario

---

## ✅ Conclusion

The fuzzy logic controller successfully models gradual and safe decision-making for robot navigation based on obstacle distance. The system demonstrates smooth transitions, robustness to uncertain input, and ease of rule modification.
