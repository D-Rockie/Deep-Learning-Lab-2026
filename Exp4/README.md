# Experiment 4 — CNN Architectures & Transfer Learning

CS3807 Deep Learning Laboratory, Shiv Nadar University Chennai.

CIFAR-10 classification using an ImageNet-pretrained VGG16, first with a frozen
base and then with the last convolution block fine tuned. LeNet-5 and AlexNet are
trained from scratch, and InceptionV3 and ResNet50 are run through the same
pipeline for comparison.

## Files

| File | What it is |
|---|---|
| `DLexp4_fast.ipynb` | The full experiment (Tasks 1–5, hyperparameter study, architecture comparison) |
| `Experiment_4.tex` | The report — theory, results, inferences, discussion answers |
| `requirements.txt` | Python dependencies |

## Running the notebook

Open in Google Colab and set **Runtime > Change runtime type > T4 GPU**, then run
all cells. Takes roughly 10–15 minutes. It works on CPU but will be much slower.

Locally:

```bash
pip install -r requirements.txt
jupyter notebook DLexp4_fast.ipynb
```

## Building the report

Upload `Experiment_4.tex` to Overleaf, create an `images/` folder, and add the
plot screenshots as `.jpg`. The expected file names are listed in a comment block
at the top of the `.tex`.

## Results

| Model | Accuracy |
|---|---|
| LeNet-5 (scratch) | 50.67% |
| AlexNet (scratch) | 69.90% |
| InceptionV3 (frozen base) | 68.85% |
| ResNet50 (transfer + fine-tune) | 84.58% |
| VGG16 (transfer + fine-tune) | **85.33%** |

Fine tuning the last block added 9.73 points over the frozen base (75.60% → 85.33%).
