# Crossword Puzzle Solver (CSP)

A constraint satisfaction–based crossword puzzle solver that fills a crossword grid using logical inference and backtracking search.

The solver models the crossword as a **Constraint Satisfaction Problem (CSP)** and applies techniques such as **node consistency**, **arc consistency (AC-3)**, and **backtracking search** to find a valid assignment of words.

---
<p align="center">
  <img src="output.png" width="500">
</p
  
## Overview

The crossword is represented as a set of variables, where each variable corresponds to a word slot in the puzzle. Each variable has:
- A position
- A direction (across or down)
- A fixed length
- A domain of possible words

The solver progressively reduces domains and assigns words while enforcing consistency constraints between overlapping word slots.

---
>

## Key Concepts Used

- Constraint Satisfaction Problems (CSPs)
- Node consistency
- Arc consistency (AC-3 algorithm)
- Backtracking search
- Constraint propagation
- Variable overlap constraints

---

## Project Structure
```
crossword/
├── assets/
├── data/
├── crossword.py
├── generate.py
└── README.md
```
---

## How the Solver Works

1. **Modeling the Problem**
   - Each word slot in the crossword is treated as a variable
   - Domains consist of all words of matching length

2. **Node Consistency**
   - Words that do not match a variable’s length are removed from its domain

3. **Arc Consistency (AC-3)**
   - Domains are further reduced by enforcing consistency between overlapping variables

4. **Backtracking Search**
   - The solver assigns words recursively
   - Assignments are checked for consistency at each step
   - Backtracking occurs when constraints are violated

5. **Solution Output**
   - If a complete consistent assignment is found, the crossword is filled and displayed
   - If no solution exists, the solver reports failure

---

## Usage

The solver is designed to be run with:
- A crossword structure file
- A word list file

When executed, the program attempts to fill the crossword using logical inference and search, printing the solution or reporting that no solution exists.

---

## Academic Context

**NOTE: This project was developed as part of Harvard’s CS50 Introduction to Artificial Intelligence with Python.**

The provided framework defines the crossword structure and variable representation.  
The constraint satisfaction logic, inference procedures, and backtracking solver were implemented by the author.

This repository is shared for **educational and portfolio demonstration purposes only** and is **not intended for reuse as coursework solutions**.

---
