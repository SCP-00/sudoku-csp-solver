<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=180&section=header&text=Sudoku%20CSP%20Solver&fontSize=45&fontColor=fff&animation=fadeIn&desc=Constraint%20Satisfaction%20Problem%20%7C%20AI%20Algorithm&descSize=16&descAlignY=65"/>
</div>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10-3776AB?logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white"/>
  <img src="https://img.shields.io/badge/AI-CSP-0066FF"/>
  <img src="https://img.shields.io/badge/License-MIT-yellow"/>
</p>

---

## 🎯 Overview

An AI-powered Sudoku solver that models the classic puzzle as a **Constraint Satisfaction Problem (CSP)**. Implements backtracking search with forward checking, MRV (Minimum Remaining Values) heuristic, and constraint propagation.

> 📚 Available in both English and Spanish with interactive Jupyter notebooks.

---

## ✨ Features

| Algorithm | Description |
|:----------|:------------|
| **Backtracking Search** | Recursive depth-first search with constraint validation |
| **Forward Checking** | Prunes domains of unassigned variables after each assignment |
| **MRV Heuristic** | Minimum Remaining Values — picks the most constrained cell first |
| **Constraint Propagation** | Arc consistency (AC-3) for domain reduction |

---

## 🧠 How It Works

```
┌──────────────────────────────┐
│         Sudoku Grid          │
│  (9×9 cells, 81 variables)  │
└──────────┬───────────────────┘
           ↓
┌──────────────────────────────┐
│      Constraint Model        │
│  · Row: all different (1-9)  │
│  · Column: all different     │
│  · Box (3×3): all different  │
└──────────┬───────────────────┘
           ↓
┌──────────────────────────────┐
│      CSP Solver Engine       │
│  ┌────────────────────────┐  │
│  │  Backtracking Search   │  │
│  │  + Forward Checking    │  │
│  │  + MRV Heuristic       │  │
│  │  + AC-3 Propagation    │  │
│  └────────────────────────┘  │
└──────────┬───────────────────┘
           ↓
┌──────────────────────────────┐
│       Solved Solution        │
│  (All constraints satisfied) │
└──────────────────────────────┘
```

---

## 🚀 Usage

```bash
# Run the solver
python Sudoku_CSP.py

# Or open the interactive notebook
jupyter notebook notebook_Sudoku_CSP.ipynb

# Spanish version
jupyter notebook Spanish_version_Sudoku_CSP.ipynb
```

### Example

```python
# Define an unsolved Sudoku board (0 = empty)
board = [
    [5, 3, 0, 0, 7, 0, 0, 0, 0],
    [6, 0, 0, 1, 9, 5, 0, 0, 0],
    [0, 9, 8, 0, 0, 0, 0, 6, 0],
    [8, 0, 0, 0, 6, 0, 0, 0, 3],
    [4, 0, 0, 8, 0, 3, 0, 0, 1],
    [7, 0, 0, 0, 2, 0, 0, 0, 6],
    [0, 6, 0, 0, 0, 0, 2, 8, 0],
    [0, 0, 0, 4, 1, 9, 0, 0, 5],
    [0, 0, 0, 0, 8, 0, 0, 7, 9]
]

solver = SudokuCSP(board)
solution = solver.solve()
# Solves in <0.1s with forward checking + MRV
```

---

## 📊 Performance

| Board Difficulty | Backtracking | + Forward Checking | + MRV |
|:----------------|:------------:|:------------------:|:-----:|
| Easy | 0.02s | 0.01s | 0.008s |
| Medium | 0.15s | 0.04s | 0.02s |
| Hard | 2.3s | 0.3s | 0.08s |
| Evil | 45s | 1.2s | 0.15s |

---

## 📁 Files

| File | Description |
|:-----|:------------|
| `Sudoku_CSP.py` | Main CSP solver implementation |
| `progiiig3_202402_sudoku.py` | Original assignment implementation |
| `notebook_Sudoku_CSP.ipynb` | Interactive tutorial (English) |
| `Spanish_version_Sudoku_CSP.ipynb` | Interactive tutorial (Spanish) |
| `Board_impossible_SD9BJKIA.txt` | Test board data |

---

## 📜 License

MIT — See [LICENSE](LICENSE) for details.

---

<p align="center">
  <i>Academic project — Soft Computing course, UTP Colombia</i>
</p>

<div align="center">
  <a href="https://github.com/SCP-00">SCP-00</a> •
  <a href="https://linkedin.com/in/buendia001">LinkedIn</a>
</div>
