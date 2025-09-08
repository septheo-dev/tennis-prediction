# Tennis Predictions (ELO-based)

This project explores tennis match outcome prediction using an ELO-style rating system. It includes a Jupyter notebook for analysis, historical ELO evolution, and sample cleaned datasets to reproduce results quickly.

## Project structure

- `main.ipynb`: End-to-end notebook for loading data, computing/updating ELO, and evaluating predictions
- `tennis_data_cleaned.csv`: Cleaned match-level dataset used as the primary input
- `data_test_ELO.csv`: Dataset with derived ELO features for testing/evaluation
- `elo_history.csv`: Long-format history of players' ELO ratings over time
- `ELO 4 players.png`: Example visualization of ELO trends for four players

## Getting started

### 1) Requirements

- Python 3.9+ (3.11+ recommended)
- Jupyter (Lab or Notebook)

Core Python packages typically used:

- pandas, numpy, matplotlib/seaborn
- scikit-learn (for train/test split, metrics, optional models)

Install with pip (example):

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\\Scripts\\activate
pip install --upgrade pip
pip install jupyter pandas numpy matplotlib seaborn scikit-learn
```

### 2) Open the notebook

From the project directory:

```bash
jupyter lab
```

Then open `main.ipynb` and run the cells in order.

## Data notes

- The CSV files in this repo are provided to reproduce the ELO computation and evaluation quickly. If you have your own raw data, adapt the loading/cleaning steps in the notebook.
- Column names in `tennis_data_cleaned.csv` should align with the notebook expectations (player identifiers, dates, outcomes, etc.).

## Method overview

- Initialize per-player ELO (e.g., 1500) and update after each match using standard ELO formulas.
- Optional features include surface adjustments, aging/decay, K-factor tuning.
- Predictions are generated from the ELO difference between players.

## Reproduce results

1. Ensure dependencies are installed.
2. Launch Jupyter and open `main.ipynb`.
3. Execute cells to compute ELO ratings and evaluate predictions on `data_test_ELO.csv`.

## Visualization

- Example ELO trajectories (see `ELO 4 players.png`).
- The notebook includes code to plot player ELO over time.

## Tips

- If you add new data, regenerate `elo_history.csv` by rerunning the notebook from scratch.
- Tune the K-factor and any decay terms in one place to keep experiments comparable.

## License

MIT
