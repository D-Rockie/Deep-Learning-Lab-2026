# DL Lab — Experiment 5

CS3807 Deep Learning Laboratory, Shiv Nadar University Chennai.

Study of weight initialization, regularization, optimizers, hyperparameter
tuning, transfer learning and 5-fold cross-validation, using MobileNetV2 on
the Oxford-IIIT Pet dataset (37 breeds).

## Files

| File | Description |
|---|---|
| `DLExp5_.ipynb` | Notebook with all the code |
| `DL_Experiment5_Report.tex` | Report (LaTeX, compiles on Overleaf) |
| `figures/` | All plots and output images |
| `requirements.txt` | Dependencies |

## Run

```bash
pip install -r requirements.txt
jupyter notebook DLExp5_.ipynb
```

A GPU is recommended. The dataset downloads automatically on first run.

## Result

Final model: frozen-base MobileNetV2 — **89.62 % test accuracy**,
5-fold CV 91.88 ± 0.86 %.
