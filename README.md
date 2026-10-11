# Job Shop Scheduling Interactive Lab

An interactive, web-based Mixed Integer Programming (MIP) and Operations Research learning platform designed for **Production Management & Variability** at the University of Mannheim.

This application provides a hands-on sandbox for visualising job shop scheduling Gantt charts, evaluating disjunctive Big-M constraints, testing JIT/perishable penalty functions, and practicing advanced formulation logic for exam preparation.

---

## 📌 Executive Summary / PRD

### 1. Product Overview
- **Name**: OPM 5610 Job Shop Scheduling Lab
- **Author**: Anne Philippi (MSc Student in Operations & Supply Chain Management, University of Mannheim)
- **Goal**: Bridge the gap between abstract mathematical formulations and intuitive graphical schedule evaluation.

---

## 🎯 Key Features

### 1. Interactive Gantt Chart Canvas
- **Visual Tracks**: Real-time rendering of processing operations across machines $M_1, M_2, M_3$.
- **Drag & Nudge Controls**: Move operations along time slots to instantly test feasible vs. infeasible schedules.
- **Feasibility Engine**: Real-time validation for:
  - Job technological precedence constraints.
  - Non-overlapping machine capacity constraints.
  - Preventive maintenance shutdown windows.

### 2. Live Mathematical Evaluation Tabs
- **Big-M & Disjunctive Formulation**: Dynamic slider for parameter $\text{bigM}$ with live pass/fail evaluation of binary disjunctive bounds ($Y_{ij}^\alpha \in \{0, 1\}$).
- **Maintenance Window (Task 1b.i)**: Interactive toggle to enforce machine clear deadline $t^*$ on target machine $\alpha^*$.
- **Dairy Factory JIT Sandbox (Task 1b.ii)**: Real-time calculation of total earliness storage ($q_j \cdot E_j$) and tardiness penalty ($u_j \cdot T_j$) costs.
- **Tardiness Extensions (Task 1c)**: Interactive toggles to switch objective criteria between:
  1. Minimizing Maximum Tardiness ($\min T_{\max}$)
  2. Minimizing Average Tardiness ($\min \frac{1}{J}\sum T_j$)
  3. Minimizing Number of Tardy Jobs ($\min \sum U_j$)

### 3. Formulation Practice (Exam Prep Module)
- **10 Advanced Challenges**: Covers real-world / non-standard scheduling extensions:
  - Sequence-dependent setup times ($s_{ij}^\alpha$)
  - Unscheduled machine breakdown windows
  - No-wait transfer constraints
  - Perishability / maximum shelf-life limits ($W_j$)
  - Machine capability eligibility restrictions
  - Upper-bounded job tardiness ($\bar{T}_j$)
  - Minimum transfer lead times ($L_{j\alpha\bar{\alpha}}$)
  - Common batch processing start times
  - Holding & setup budget constraints ($B$)
  - Maintenance window disjunctive choices
- **Dynamic Shuffling Engine**: Features a Fisher-Yates algorithm that shuffles multiple-choice options upon reset so correct answers are randomized every time.
- **KaTeX Mathematical Typesetting**: Full LaTeX equation rendering (using proper `\text{bigM}` syntax) with instant step-by-step explanations.

---

## 🏗️ Technical Architecture & Tech Stack

- **Frontend**: Single-file, standalone zero-build web application (`index.html`).
- **Styling**: Tailwind CSS CDN.
- **Math Rendering**: KaTeX CDN (v0.16.9) with auto-render extension.
- **Language**: Pure Vanilla JavaScript (ES6+).
- **Deployment**: Compatible with GitHub Pages, Netlify, or direct local browser execution.

---

## 🚀 Quick Start & Usage

### Running Locally
No build step or `npm install` required!

1. Clone this repository:
   ```bash
   git clone [https://github.com/anne-philippi/job-shop-lab.git](https://github.com/anne-philippi/job-shop-lab.git)
