
<p align="center"> <img src="fig/logo.jpg" style="width: 70%;" id="title-icon"></p>

<p align="center" style="display: flex; flex-direction: row; justify-content: center; align-items: center">
📄 <a href="" target="_blank" style="margin-right: 15px; margin-left: 10px">Paper</a> • 
🤗 <a href="" target="_blank" style="margin-left: 10px">Dataset</a> 
</p>

Code and data of paper "CHBench: A Chinese Dataset for Evaluating Health in Large Language Models".

## Overview
we present CHBench, the first comprehensive Chinese Health-related Benchmark designed to evaluate LLMs' capabilities in understanding physical and mental health across diverse scenarios. CHBench includes 6,493 entries related to mental health and 2,999 entries focused on physical health, covering a broad spectrum of topics.
The collectiong steps are outlined below.
<p align="center"> <img src="fig/creationProcess.jpg" style="width: 85%;" id="title-icon"></p>


## Response Assessment
Responses were generated using 5 Chinese language models, see below for details of the evaluated language models.

| **Model** | **Access** | **Version**     | **Creator**   |
|:---------:|:----------:|:---------------:|:-------------:|
| ERNIE Bot | api        | ERNIE-4.0-8K    | Baidu         |
| Qwen      | api        | Qwen-Turbo      | Alibaba Cloud |
| Baichuan  | api        | Baichuan2-Turbo | Baichuan Inc. |
| ChatGLM   | api        | GLM-4           | Tsinghua & Zhipu |
| SparkDesk | api        | Spark3.5 Max    | iFLYTEK       |


### Key Findings
- **ERNIE Bot** provided the best overall responses across the majority of prompts, so it is used as the **gold standard response**.
- **Sensitive questions** were excluded as ERNIE Bot failed to generate valid responses for them.
- **Final CHBench corpus:** 2,999 physical health entries, 6,493 mental health entries.

⚠️ Caution: This content may include model outputs that could be perceived as offensive.

### Analysis of Similarity in Physical Health

<p align="center"> <img src="fig/physicalSim.jpg" style="width: 85%;" id="title-icon"></p>

ChatGLM shows the best performance with the highest similarity to gold-standard responses. Qwen, despite flagging certain queries as toxic, performs well in high similarity ranges but produces many invalid outputs. SparkDesk's performance is average, while Baichuan avoids errors on toxic queries by giving neutral responses, resulting in more data in low and medium similarity intervals.


### Analysis of Similarity in Mental Health


<p align="center"> <img src="fig/mentalSim.jpg" style="width: 85%;" id="title-icon"></p>

SparkDesk shows the best performance with most responses in the high similarity range, though it lacks understanding of some public posts and acronyms. ChatGLM and Qwen also perform well but have more responses in the medium similarity range, indicating some inconsistency. Qwen is more sensitive to data, often flagging content as toxic. Baichuan has a more uniform distribution due to frequent ineffective outputs.



## Citation
If you finding our work interesting or helpful to you, please cite this repo.
... ...
```

```
