
This repository contains a single Jupyter Notebook:
- `mlpc_code-group.ipynb`: Core implementation of the smart grid optimization using Genetic Algorithms and parallel computing (`joblib`).

---

## Features

- Genetic Algorithm for smart grid load balancing.
- Chromosome encoding, fitness evaluation, selection, crossover, and mutation logic.
- Parallel computation using `joblib.Parallel` for speedup in fitness evaluations.
- Real-time benchmarking between serial and parallel execution.
- Visualization of GA performance across generations.

---

## Requirements

To run this notebook, ensure you have the following Python packages installed:

```bash
pip install numpy pandas matplotlib joblib
```

If using Google Colab, it supports most of the requirements out of the box.

---

## Dataset

Please provide a CSV file named `smart_grid_dataset.csv`. This file should contain the smart grid data to be optimized. The code supports upload via:

- **Google Colab**: Uses `files.upload()` for user file input.
- **Local Environment**: Use a `smart_grid_dataset.csv` file in the working directory.

---

## How to Run

1. Open the notebook: `mlpc_code-group.ipynb`
2. Run each cell sequentially.
3. Upload the `smart_grid_dataset.csv` when prompted.
4. The code will:
   - Load and preprocess the data.
   - Run GA in both serial and parallel modes.
   - Compare their performances using visual plots and execution time.

---

## Main Components

- `load_smart_grid_dataset()`: Loads dataset.
- `initialize_population()`: Randomly initializes the GA population.
- `fitness_function()`: Measures efficiency of each chromosome (energy distribution configuration).
- `crossover() & mutate()`: Implements GA operators.
- `run_serial_ga()` vs `run_parallel_ga()`: Compares single-core and multi-core execution using `joblib`.

---

## Output

- Prints best solutions and fitness values.
- Plots GA convergence.
- Displays time comparison between serial and parallel versions.

---