## 📑 Agile Project Simulation & Risk Analysis

### 🚀 Project Overview

This repository implements a **simulation-based approach** to optimize **Agile software delivery** in a multi-team setup. It uses **sprint modeling**, **Monte Carlo simulation**, and **sensitivity analysis** to provide data-driven forecasts for project completion time and cost, and to evaluate the impact of crucial factors like **technical debt** and **project risks**.

The overall goal is to provide **data-driven recommendations** for efficient project planning, resource allocation, and risk mitigation in complex Agile environments.

---

### 📁 Repository Structure

The project structure is organized to clearly separate code, data, and visualizations.
Agile_Project_Simulation/
│
├── Agile_Simulation.ipynb         # Main Jupyter Notebook performing all simulations and analysis
├── sprint_results.csv             # Detailed sprint-by-sprint simulation outputs
├── monte_carlo_completion.csv     # Results of all Monte Carlo simulation runs
├── sensitivity_analysis.csv       # Data from sensitivity analysis experiments
├── charts/                        # Visualization charts (burndown, velocity trends, histograms, flow diagram, etc.)
│ ├── burndown.png                 # Burndown chart visualizing remaining work
│ ├── velocity_trend.png           # Trend of team velocity across sprints
│ ├── earned_value.png             # Earned Value Analysis plot
│ ├── completion_histogram.png     # Distribution of project completion times from Monte Carlo
└── README.md                      # Project description and usage instructions

---
### 🔧 Requirements & Setup

This project is built using **Python 3.x** and relies on standard data-science libraries.

#### **Dependencies**

The core libraries required include: `pandas`, `numpy`, `matplotlib`, and `seaborn`.

#### **Installation**

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/Abdulmoiz-25/Agile_Project_Simulation.git](https://github.com/Abdulmoiz-25/Agile_Project_Simulation.git)
    cd Agile_Project_Simulation
    ```

2.  **Install dependencies:**
    If a `requirements.txt` is present:
    ```bash
    pip install -r requirements.txt
    ```
    Otherwise, install manually:
    ```bash
    pip install pandas numpy matplotlib seaborn
    ```

3.  **Run the simulation:**
    Open the main notebook and execute all cells to generate output files and charts:
    ```bash
    jupyter notebook Agile_Simulation.ipynb
    ```

---

### 🧪 What’s Inside

The core of the simulation covers three major analytical techniques:

#### 1. Sprint Simulation & Modeling
* Models **team velocities** with inherent **randomness**.
* Incorporates the impact of **technical debt**, causing a reduction in effective team velocity.
* Simulates **resource contention** and **sprint-wise backlog burn-down** for a multi-team project.

#### 2. Monte Carlo Simulation & Risk Analysis
* Performs repeated simulation runs (e.g., 100 runs) incorporating **defined risk probabilities** (e.g., scope creep, member departure, integration issues).
* Estimates the **probable completion sprints** and the associated **project cost** distribution.

#### 3. Sensitivity Analysis
* Systematically explores how varying key input parameters (team velocities, technical debt factors, risk probabilities) impact the overall project completion time and cost.
* **Identifies high-impact parameters** that deserve focused management attention.

#### 4. Visualizations
The `charts/` folder contains key visual artifacts: Burndown charts, velocity trends, earned value analysis, Monte Carlo outcome histograms, and a simulation flow diagram.

---

### 📊 Key Findings & Recommendations

Based on the default simulation parameters, the following findings and recommendations are generated:

* **Reduce technical debt early:** Proactive investment improves effective velocity and minimizes project delays.
* **Invest more in high-impact teams (e.g., Team Alpha):** Increasing capacity/efficiency in high-throughput teams has the biggest effect on overall project completion.
* **Proactively mitigate risks:** Lowering the probability or impact of defined risks reduces schedule uncertainty and variance.
* **Avoid mid-sprint scope changes:** Minimizes volatility and significantly improves predictability.

**Overall Impact:** Applying these recommendations is projected to reduce the project completion by approximately **1–2 sprints** and significantly lower the probability of cost overruns.

---

### 🎯 How to Use / Extend

This repository is designed to be a flexible tool for Project Managers and Analysts.

* **Adapt Parameters:** Modify team parameters (initial velocity, cost per sprint), overall backlog size, risk probabilities, and technical debt factors within the `Agile_Simulation.ipynb` notebook to reflect different project scenarios.
* **What-If Analysis:** Run multiple Monte Carlo simulations with different assumptions to compare various outcome scenarios.
* **Reporting:** Use the generated data (`*.csv` files) and charts (`charts/` folder) directly for project status reporting or proposal documentation.

---
