# Experiment 6 - RNN, LSTM, GRU for Sequence Learning and Video Understanding


**Covers:** UCI HAR activity classification with SimpleRNN / LSTM / GRU on raw
(N, 128, 9) inertial signals, BPTT numerical check, sequence-length study,
CNN(MobileNetV2)-LSTM/GRU video action recognition on a UCF101 subset, and an
encoder-decoder sequence-reversal task.

**Run (Kaggle):** import the notebook, enable GPU + Internet, attach a UCF101
dataset containing the original `.avi` clips, then Run All. UCI HAR downloads
automatically.

**Run (local):** `pip install -r requirements.txt`, set `INPUT_DIR` / `WORK_DIR`
in cell 1 to local paths, then run all cells.

