# DeViBench: The first benchmark evaluates how video quality affects MLLM accuracy.

This repository maintains the **DeViBench** (**De**graded **Vi**deo Understanding **Bench**mark) from the HotNets paper **"Chat with AI: The Surprising Turn of Real-time Video Communication from Human to AI"**.

*The benchmark is continuously growing, and we are considering transforming more existing Streaming Video Understanding Benchmarks to the "DeViBench style".


<div style="text-align: center;">
  <img src="docs/teaser.png" width="512">
</div>
&nbsp;
<div style="text-align: center;">
  <img src="docs/bitrate_reduce_accuracy.png" width="512">
</div>

## 📁 Dataset Content

The dataset file `datasets.csv` contains the following columns:

| Column | Description |
|--------|-------------|
| `sample_folder` | Corresponding video ID. This dataset uses the same video files as the [StreamingBench Real-Time Visual Understanding](https://huggingface.co/datasets/mjuicem/StreamingBench/tree/main) dataset, available for download from the provided link. |
| `start_time` | Start time of the video segment. Questions refer to a 5-second segment starting from this timestamp. |
| `question` | The question content. |
| `options` | Available options for the question. |
| `standard_answer` | Standard answer to the question. |
| `task_type` | Task type of the question. |


The prompt format for asking questions:
```
You are a multiple-choice question answering assistant.
Your task is to output only the letter of the correct option, without any explanation or extra text.
Question:
[Question]
Options:
[Options]
```

## 📥 Data Download

Video files can be downloaded from:

> https://huggingface.co/datasets/mjuicem/StreamingBench/tree/main

Please match the video files with the corresponding `sample_folder` in `datasets.csv`.

## 📊 Distribution of our generated QA samples

<div style="text-align: center;">
  <img src="docs/benchmark_detail.png" width="512">
  <p><strong>Outer ring: QA categories. Inner ring: Whether the
question requires multiple frames to answer.</strong></p>
</div>

An example (200 kbps vs 2000 kbps):






https://github.com/user-attachments/assets/d81af6fd-95b2-40f2-9ef0-5acc473e88cd






**Question**: How does the road gradient (GRAD) change as the cyclist progresses?

**Options**: 

* (A) Remains constant at -1 

* (B) Gradually becomes more negative 

* (C) Fluctuates between -1 and -2 

* (D) Gradually becomes less negative

**Answer**: B

## 🔧 Pipeline for automatic QA sample construction

<div style="text-align: center;">
  <img src="docs/sample_generation.png" width="512">
</div>

## 📝 Citation
```
@article{wu2025chat,
  title={Chat with AI: The Surprising Turn of Real-time Video Communication from Human to AI},
  author={Wu, Jiangkai and Ren, Zhiyuan and Liu, Liming and Zhang, Xinggong},
  journal={arXiv preprint arXiv:2507.10510},
  year={2025}
}
```

## ⚠️ Important Note

The data is model-generated and may contain minor errors. We recommend using it primarily for exploratory analysis and demonstration purposes.




