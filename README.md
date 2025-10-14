# DeViBench

This repository provides a sample implementation of the **DeviBench** dataset from the paper **"Chat with AI: The Surprising Turn of Real-time Video Communication from Human to AI"**.

## 📁 Dataset Content

The dataset file `datasets.csv` contains the following columns:

| Column | Description |
|--------|-------------|
| `sample_id` | Corresponding video ID. This dataset uses the same video files as the [StreamingBench Real-Time Visual Understanding](https://huggingface.co/datasets/mjuicem/StreamingBench/tree/main) dataset, available for download from the provided link. |
| `start_time` | Start time of the video segment. Questions refer to a 5-second segment starting from this timestamp. |
| `question` | The question content. |
| `options` | Available options for the question. |
| `standard_answer` | Standard answer to the question. |
| `task_type` | Task type of the question. |

## 📥 Data Download

Video files can be downloaded from:

> https://huggingface.co/datasets/mjuicem/StreamingBench/tree/main

Please match the video files with the corresponding `sample_id` in `datasets.csv`.

## ⚠️ Important Note

**This dataset is currently not suitable for rigorous evaluation.** The data is model-generated and may contain minor errors. We recommend using it primarily for exploratory analysis and demonstration purposes.

