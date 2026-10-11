# OPM 5610: Job Shop Scheduling Interactive Lab

An interactive, web-based Mixed Integer Programming (MIP) and Operations Research learning platform designed for **OPM 5610 (Production Management & Variability)** at the University of Mannheim.

This application provides a hands-on sandbox for visualising job shop scheduling Gantt charts, evaluating disjunctive Big-M constraints, testing JIT/perishable penalty functions, and practicing advanced formulation logic for exam preparation.

🚀 **Live Interactive Demo**: [https://job-shop-lab.vercel.app](https://job-shop-lab.vercel.app)

---

## 📌 Executive Summary / PRD

### 1. Product Overview
- **Name**: OPM 5610 Job Shop Scheduling Lab
- **Live URL**: [job-shop-lab.vercel.app](https://job-shop-lab.vercel.app)
- **Author**: Anne Philippi (MSc Student in Operations & Supply Chain Management, University of Mannheim)
- **Goal**: Bridge the gap between abstract mathematical formulations and intuitive graphical schedule evaluation.

---

## 🎯 Key Features

### 1. Interactive Gantt Chart Canvas
- **Visual Tracks**: Real-time rendering of processing operations across machines *M*₁, *M*₂, *M*₃.
- **Drag & Nudge Controls**: Move operations along time slots to instantly test feasible vs. infeasible schedules.
- **Feasibility Engine**: Real-time validation for:
  - Job technological precedence constraints.
  - Non-overlapping machine capacity constraints.
  - Preventive maintenance shutdown windows.

### 2. Live Mathematical Evaluation Tabs
- **Big-M & Disjunctive Formulation**: Dynamic slider for parameter *bigM* with live pass/fail evaluation of binary disjunctive bounds (*Y*<sub>*ij*</sub><sup>*α*</sup> ∈ {0, 1}).
- **Maintenance Window (Task 1b.i)**: Interactive toggle to enforce machine clear deadline *t*\* on target machine *α*\*.
- **Dairy Factory JIT Sandbox (Task 1b.ii)**: Real-time calculation of total earliness storage (*q*<sub>*j*</sub> · *E*<sub>*j*</sub>) and tardiness penalty (*u*<sub>*j*</sub> · *T*<sub>*j*</sub>) costs.
- **Tardiness Extensions (Task 1c)**: Interactive toggles to switch objective criteria between:
  1. Minimizing Maximum Tardiness (min *T*<sub>max</sub>)
  2. Minimizing Average Tardiness (min <sup>1</sup>/<sub>*J*</sub> Σ *T*<sub>*j*</sub>)
  3. Minimizing Number of Tardy Jobs (min Σ *U*<sub>*j*</sub>)

### 3. Formulation Practice (Exam Prep Module)
- **10 Advanced Challenges**: Covers real-world / non-standard scheduling extensions:
  - Sequence-dependent setup times (*s*<sub>*ij*</sub><sup>*α*</sup>)
  - Unscheduled machine breakdown windows
  - No-wait transfer constraints
  - Perishability / maximum shelf-life limits (*W*<sub>*j*</sub>)
  - Machine capability eligibility restrictions
  - Upper-bounded job tardiness (*T̄*<sub>*j*</sub>)
  - Minimum transfer lead times (*L*<sub>*jαᾱ*</sub>)
  - Common batch processing start times
  - Holding & setup budget constraints (*B*)
  - Maintenance window disjunctive choices
- **Dynamic Shuffling Engine**: Features a Fisher-Yates algorithm that shuffles multiple-choice options upon reset so correct answers are randomized every time.
- **KaTeX Mathematical Typesetting**: Full LaTeX equation rendering in the app UI with instant step-by-step explanations.

---

## 🏗️ Technical Architecture & Tech Stack

- **Frontend**: Single-file, standalone zero-build web application (`index.html`).
- **Styling**: Tailwind CSS CDN.
- **Math Rendering**: KaTeX CDN (v0.16.9) with auto-render extension.
- **Language**: Pure Vanilla JavaScript (ES6+).
- **Deployment**: Hosted on **Vercel** with continuous deployment from `main`.

---

## 🚀 Quick Start & Deployment

### Access Online
Experience the live web app directly in your browser:
👉 **[job-shop-lab.vercel.app](https://job-shop-lab.vercel.app)**

### Running Locally
No build step or `npm install` required!

1. Clone this repository:
   ```bash
   git clone [https://github.com/anne-philippi/job-shop-lab.git](https://github.com/anne-philippi/job-shop-lab.git)
