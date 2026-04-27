# Metric Methods: WIne Classification

Metric classification with kNN and distance-based methods on the Wine dataset — built with **STEP flow ALIGN** methodology.

## 🧩 A.L.I.G.N. — alignment

- **A** — classify Wine species with metric methods (kNN, distances, window functions)
- **L** — sklearn Wine, hold-out, cross-validation, hyperparameter search
- **I** — Python + scikit-learn + matplotlib
- **G** — data exploration → kNN from scratch → evaluation → visualization
- **N** — confirmed? ✓

## 🚶 S.T.E.P. — execution

- **S** — load and split data
- **T** — test with k=3 on train sample
- **E** — implement and log results
- **P** — proceed to parameter search

## 📊 Results

| Method | Accuracy |
|--------|----------|
| kNN (k=5) | 96.7% |
| ... | ... |

## 🧠 Follows

- **STEP flow ALIGN** — methodology for conscious development  
  → [manifoldmind/S-T-E-P-flow-A-L-I-G-N](https://github.com/manifoldmind/S-T-E-P-flow-A-L-I-G-N)

## 📁 Project structure
```
Metric-Methods--Wine-Classifications/
├── .obsidian/ # конфигурация Obsidian (личные заметки)
├── .vscode/ # настройки VS Code
├── ALIGN.md # методология A.L.I.G.N. с "огранкой" ключевых терминов ML
├── STEP.md # полный отчёт по лабораторной работе (EDA → kNN → CV)
├── DEEP — Теория по accuracy.md # теория метрики accuracy, формула, ограничения
├── DEEP — Теория по кросс-валидации.md # описание кросс-валидации, k-fold, выборка
├── DEEP — Алгоритм псевдослучайных чисел.md # заметки о псевдослучайных числах и random_state
├── DONE.ipynb # основной рабочий ноутбук с кодом и результатами
├── __sandbox.ipynb # черновик / песочница для экспериментов
├── curr state.md # #CHILLOUT-анализ текущего результата (K=7, дальнейшие шаги)
├── requirements.txt # список зависимостей Python
├── README.md # этот файл
├── Pasted image 20260426211115.png # скриншот / изображение (приложено к проекту)
└── tmp.md # временные заметки
```


## Description

This repository implements **metric classification** on the classic **Wine dataset** using the k‑Nearest Neighbors (kNN) algorithm and various distance‑based methods. The entire workflow is built around the **STEP flow ALIGN** methodology — a structured approach that keeps the development process transparent, reproducible, and beginner‑friendly.

### Key features

- **kNN from scratch** using `scikit-learn`’s `KNeighborsClassifier`
- **Hyperparameter tuning** – grid‑search over `k` with hold‑out and cross‑validation
- **Different distance metrics** (Euclidean, Manhattan, etc.)
- **Window functions** (uniform, distance‑weighted) to weight neighbor votes
- **Visual evaluation** – accuracy plots, confusion matrix, decision boundaries

## Dataset

The **Wine dataset** (178 samples, 13 numerical features, 3 classes) is loaded from `sklearn.datasets.load_wine()`. It represents chemical analyses of wines grown in three different Italian regions. The classes are balanced (~59/71/48), which makes **accuracy** a reasonable primary metric.

For a detailed description, see `DEEP — Теория по accuracy.md`.

## Requirements

Install the dependencies listed in `requirements.txt`:

```bash
pip install -r requirements.txt
```

Minimum versions:

numpy >= 1.21.0

pandas >= 1.3.0

scikit-learn >= 1.0.0

matplotlib >= 3.5.0

seaborn >= 0.11.0

jupyter >= 1.0.0

## How to run

1. **Clone the repository**
   ```bash
   git clone https://github.com/manifoldmind/Metric-Methods--Wine-Classifications.git
   cd Metric-Methods--Wine-Classifications
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Open the main notebook**
   ```bash
   jupyter notebook DONE.ipynb
   ```

4. **Run all cells** to reproduce the complete pipeline: data loading → EDA → hold‑out kNN → cross‑validation → visualization.

> ℹ️ **Tip:** `__sandbox.ipynb` contains experimental code and intermediate tests — useful for understanding the trial‑and‑error process.

## Results

| Method | Accuracy (test) |
|--------|-----------------|
| kNN (k=5) | 96.7% |
| kNN (k=7, hold‑out) | ~96.7% |
| kNN (k=7, 5‑fold CV) | ~96.1% ± 2.5% |

*Detailed results, including per‑fold CV scores and hyperparameter sensitivity plots, are available in `DONE.ipynb`.*

## Follows

- **STEP flow ALIGN** — methodology for conscious development → [manifoldmind/S-T-E-P-flow-A-L-I-G-N](https://github.com/manifoldmind/S-T-E-P-flow-A-L-I-G-N)

## License

This project is publicly available as part of an educational portfolio. Feel free to use, modify, and share — attribution is appreciated.

---

*Built with ❤️ and a lot of curiosity by [Sophia Entropofugus](https://github.com/manifoldmind).*
