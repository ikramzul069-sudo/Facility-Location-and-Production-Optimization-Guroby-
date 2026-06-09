# Facility Location and Production Optimization (Gurobi)

<div align="center">
  <img src="https://img.shields.io/badge/Language-Python-blue.svg" alt="Python">
  <img src="https://img.shields.io/badge/Solver-Gurobi-red.svg" alt="Gurobi Optimizer">
  <img src="https://img.shields.io/badge/Environment-Jupyter%20Notebook-orange.svg" alt="Jupyter Notebook">
</div>

---

## 1. About This Project & File Structure

### Project Description
This project implements a Mixed-Integer Programming (MIP) model using Python and the Gurobi Optimizer to solve a complex supply chain network problem. 

The primary objective of this project is to maximize total revenue by determining the optimal strategy for:
* **Facility Location:** Deciding which facilities to open based on their geographical coordinates and capacities.
* **Production Planning:** Calculating the exact number of products to manufacture at each opened facility based on resource costs.
* **Logistics & Shipping:** Routing products from facilities to demand locations while minimizing shipping costs and respecting a strict maximum total cost budget of $500,000.

This project covers essential Operations Research (OR) and mathematical optimization concepts, including decision variable mapping, capacity bounding, supply-demand balancing, and objective function formulation.

### File Structure & Functionality
Here is a breakdown of what each file in this repository does:
* **`1. Assignment-1.ipynb`** : The main and only Jupyter Notebook file containing the complete pipeline. It includes the problem data structures (locations, requirements, costs, demands), the Gurobi model formulation (variables, constraints, objective), the optimization execution, and the final visualization of the supply chain network using Matplotlib.

---

## 2. Set-Up
Before running this project, ensure your local environment has the following dependencies installed:

1. **Python:** Python 3.x installed on your system.
2. **Jupyter Notebook:** To open and run the `.ipynb` file.
3. **Gurobi Optimizer:** The Gurobi mathematical optimization solver. **Note:** You must have a valid Gurobi license (academic or commercial) set up on your machine.
4. **Python Libraries:** Install the required packages using `pip`:
```bash
pip install gurobipy matplotlib jupyterlab
```
## 3. Compilation
Since this project uses Python and Jupyter Notebook, traditional compilation (like make or gcc) is not required. Instead, you need to launch the Jupyter environment to interpret the code.

Open your terminal in the project directory and start the Jupyter Notebook server:

```Bash
jupyter notebook
This command will open a new tab in your web browser. Click on 1. Assignment-1.ipynb to open the notebook.
```
## 4. Execution
Unlike a command-line executable, you run this simulation interactively cell by cell.

Running the Notebook:

Open the notebook in your browser.

Click on the first cell.

Press Shift + Enter to run each cell sequentially, or click "Run All" from the top menu bar to execute the entire optimization pipeline at once.

Expected Results:
Once the optimization cell (m.optimize()) finishes executing, you should see the following outputs:

Gurobi Log: The mathematical solver log detailing the optimization process, heuristics, and the MIP gap.

Optimal Solution Data: Text output confirming Optimal solution found along with the maximized Total Revenue value. It will also print exactly which facilities were chosen to open, their production amounts, and the shipped quantities to various demand nodes.

Network Visualization: A Matplotlib 2D graph popping up at the end of the notebook, visually mapping the facility locations, demand nodes, and drawing the optimal shipping routes across the grid.
