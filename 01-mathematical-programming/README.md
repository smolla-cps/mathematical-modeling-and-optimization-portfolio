# Mathematical Programming and Optimization — Python Portfolio

A collection of five executable Jupyter notebooks covering mathematical optimization models, solution algorithms, numerical calculations, and engineering decision-making. The notebooks combine **problem descriptions, mathematical formulations, algorithm explanations, pseudocode and iteration traces where applicable, Python implementations, visualizations, and interpretations of results**.

The collection is organized by method, progressing from continuous linear programming to integer and nonlinear optimization. Examples include production planning, transportation and distribution, resource allocation, project selection, routing, and constrained optimization.

## Notebooks

| Notebook | Focus | Methods and applications |
|---|---|---|
| [01 — Linear Programming: Simplex and Sensitivity Analysis](01_Linear-Programming-simplex-method-and-sensitivity-Analysis.ipynb) | LP formulation and solution methods | Graphical maximization/minimization, basic feasible solutions, Simplex tableaux, Big-M, two-phase method, special cases, graphical and algebraic sensitivity analysis, production planning |
| [02 — Linear Programming: Duality and Post-Optimal Analysis](02_Linear-Programming-duality-and-post-optimal-analysis.ipynb) | Primal–dual relationships and model changes | Dual construction, complementary slackness, basis calculations, reduced costs, shadow prices, dual Simplex, generalized Simplex concepts, RHS/objective changes, new constraints and activities |
| [03 — Transportation Models](03_Linear-Programming-transportation-model.ipynb) | Distribution and network allocation | Balanced/unbalanced transportation, production–inventory transportation models, Northwest Corner, Least Cost, Vogel's Approximation, MODI, assignment/Hungarian method, transshipment |
| [04 — Integer Linear Programming](04_Integer-Linear-Programming.ipynb) | Discrete optimization decisions | Binary capital budgeting, set covering, fixed-charge formulations, logical constraints, enumeration, branch-and-bound, Gomory cutting planes, traveling salesperson heuristics and exact search |
| [05 — Nonlinear Programming](05_Nonlinear-Programming.ipynb) | Nonlinear objectives and constraints | Dichotomous and golden-section searches, steepest ascent, separable programming, quadratic programming/KKT, chance constraints, linear-combinations method, SUMT |

## Repository Structure

```text
mathematical-programming-and-optimization/
├── README.md
├── requirements.txt
├── 01_Linear-Programming-simplex-method-and-sensitivity-Analysis.ipynb
├── 02_Linear-Programming-duality-and-post-optimal-analysis.ipynb
├── 03_Linear-Programming-transportation-model.ipynb
├── 04_Integer-Linear-Programming.ipynb
└── 05_Nonlinear-Programming.ipynb
```

## How to Run

### Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Upload a notebook or open it directly from a GitHub repository.
3. Select **Runtime → Run all** to execute the examples in order.
4. The standard Colab Python environment usually includes the main packages. If a package is missing or outdated, install the dependencies with:

   ```python
   %pip install -r requirements.txt
   ```

   The command above works when `requirements.txt` has also been uploaded to the Colab working directory. Otherwise, install packages directly with `%pip install numpy pandas matplotlib scipy`.

### Local Jupyter

**Requirements:** Python 3.10 or newer (recommended), with an installation of SciPy supporting `scipy.optimize.milp` (SciPy 1.9+).

```bash
python -m venv .venv
```

Activate the environment:

- **Windows (PowerShell):** `.venv\Scripts\Activate.ps1`
- **macOS/Linux:** `source .venv/bin/activate`

Install dependencies and start Jupyter:

```bash
python -m pip install -r requirements.txt
jupyter lab
```

Open a notebook and run its cells from top to bottom. Each notebook contains self-contained numerical models and does not require a separate input dataset.

## Portfolio Approach

Each notebook emphasizes the connection between **mathematical modeling** and **computational optimization**:

1. **Problem definition:** Describe the operational situation, data, decisions, and goals.
2. **Mathematical model:** Define decision variables, an explicit objective function, and constraints.
3. **Algorithm mechanics:** Explain why each method makes its next decision; include pseudocode and numerical traces where provided.
4. **Python implementation:** Apply numerical optimization routines or implement algorithm steps directly.
5. **Verification:** Compare analytical or algorithmic results with solver solutions, feasibility checks, or objective evaluations as applicable.
6. **Interpretation:** Connect optimal decisions, costs, resource utilization, bounds, or sensitivities to the original problem.

Figures and iteration tables are produced by notebook cells. Mathematical expressions are written in notebook Markdown using LaTeX notation.

## Python Tools

- **NumPy:** Matrix operations, numerical arrays, and algorithm calculations.
- **Pandas:** Results tables, model data, and iteration histories.
- **Matplotlib:** Feasible-region plots, convergence traces, and model visualizations.
- **SciPy:** Continuous and mixed-integer optimization (`linprog`, `milp`, `minimize`, `minimize_scalar`), assignment (`linear_sum_assignment`), probability distributions, and graph-related calculations.
- **IPython / JupyterLab:** Interactive notebook execution and formatted output.



## Intended Audience

Students, researchers, and practitioners interested in operations research, industrial engineering, mathematical programming, production and logistics optimization, and algorithm implementation in Python.
