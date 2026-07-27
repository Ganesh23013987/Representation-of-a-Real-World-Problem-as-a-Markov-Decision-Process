# Representation of a Student Study Planner as a Markov Decision Process (MDP)

## Overview

This project demonstrates how a **Student Study Planner** can be modeled as a **Markov Decision Process (MDP)**. The MDP framework is widely used in Artificial Intelligence and Reinforcement Learning to represent sequential decision-making problems.

In this project, a student's preparation for an examination is modeled using states, actions, transition probabilities, rewards, and a discount factor.

---

## Aim

To represent a Student Study Planner as a Markov Decision Process (MDP) by defining:

- State Space
- Action Space
- Transition Probability
- Reward Function
- Discount Factor
- Python Representation

---

# Problem Statement

A student plans daily study activities to prepare for examinations. Every day, the student chooses one of the following actions:

- Study
- Revise
- Practice Questions
- Take a Break

These actions affect the student's preparation level.

The objective is to select the best sequence of actions that maximizes learning and helps the student become fully prepared for the examination.

This real-world problem can be represented as a **Markov Decision Process (MDP).**

---

# MDP Components

MDP = (S, A, P, R, γ)

| Symbol | Description |
|---------|-------------|
| S | Set of States |
| A | Set of Actions |
| P | Transition Probability |
| R | Reward Function |
| γ | Discount Factor |

---

# State Space

```text
S = {
    Unprepared,
    Preparing,
    Well_Prepared,
    Exam_Ready
}
```

---

# Action Space

```text
A = {
    Study,
    Revise,
    Practice_Questions,
    Take_Break
}
```

---

# Transition Function

| Current State | Action | Next State | Probability |
|---------------|---------|------------|-------------|
| Unprepared | Study | Preparing | 0.90 |
| Preparing | Practice Questions | Well Prepared | 0.80 |
| Well Prepared | Revise | Exam Ready | 0.95 |
| Preparing | Take Break | Preparing | 1.00 |

---

# Reward Function

| Action | Reward |
|---------|-------:|
| Study | +5 |
| Revise | +4 |
| Practice Questions | +6 |
| Take Break | -2 |

---

# Discount Factor

```text
γ = 0.9
```

---

# Graphical Representation

> Add your generated MDP image inside the **images** folder.

```text
images/
    mdp_diagram.png
```

---

# Python Implementation

The Python implementation uses dictionaries to represent:

- States
- Actions
- Transition Function
- Reward Function
- Discount Factor

Run

```bash
python student_study_planner_mdp.py
```

---

# Sample Output

```text
========== Student Study Planner MDP ==========

States
------
1. Unprepared
2. Preparing
3. Well Prepared
4. Exam Ready

Actions
-------
Study
Revise
Practice Questions
Take Break

Transitions
-----------
Unprepared --Study--> Preparing | Probability = 0.9
Preparing --Practice Questions--> Well Prepared | Probability = 0.8
Well Prepared --Revise--> Exam Ready | Probability = 0.95
Preparing --Take Break--> Preparing | Probability = 1.0

Rewards
-------
Study : 5
Revise : 4
Practice Questions : 6
Take Break : -2

Discount Factor (γ): 0.9
```

---

# Result

The Student Study Planner was successfully represented as a Markov Decision Process (MDP). The Python implementation models states, actions, transition probabilities, rewards, and discount factor using dictionaries, demonstrating the application of Reinforcement Learning concepts to a real-world problem.

---

## Author

**Ganesh D**

B.Tech Artificial Intelligence and Machine Learning

Saveetha Engineering College
