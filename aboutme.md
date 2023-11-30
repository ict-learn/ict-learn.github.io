---
layout: page
title: About me
subtitle: Why you'd want to go on a date with me
---

# Papers 

- [Papers](#papers)
  - [DyVal: graph-informed dynamic evaluation of large language models](#dyval-graph-informed-dynamic-evaluation-of-large-language-models)
  - [Meta Semantic Template for Evaluation of Large Language Models](#meta-semantic-template-for-evaluation-of-large-language-models)
  - [A survey on evaluation of large language models](#a-survey-on-evaluation-of-large-language-models)
  - [PromptBench: towards evaluating the adversarial robustness to prompts of LLMs](#promptbench-towards-evaluating-the-adversarial-robustness-to-prompts-of-llms)
  - [GLUE-X: Evaluation from an Out-of-distribution Generalization Perspective](#glue-x-evaluation-from-an-out-of-distribution-generalization-perspective)
  - [PandaLM: An Automatic Evaluation Benchmark for LLM Instruction Tuning Optimization](#pandalm-an-automatic-evaluation-benchmark-for-llm-instruction-tuning-optimization)
  - [On the robustness of ChatGPT: an adversarial and OOD perspective](#on-the-robustness-of-chatgpt-an-adversarial-and-ood-perspective)


- - -

## DyVal: graph-informed dynamic evaluation of large language models

*Added on: 03/10/2023.*

<p align="center">
  Kaijie Zhu<sup>*1</sup>,
  Jiaao Chen<sup>*2</sup>,  
  Jindong Wang<sup>#1</sup>,  
  Neil Zhenqiang Gong<sup>3</sup>,  
  Diyi Yang<sup>4</sup>,
  Xing Xie<sup>1</sup>
</p>  

<p align="center">
<sup>1</sup> Microsoft Research,
<sup>2</sup> Georgia Tech,
<sup>3</sup> Duke University,
<sup>4</sup> Stanford University<br>
(*: Co-first authors, #: Corresponding author)
</p>

<p align="center">
[<a href="https://arxiv.org/pdf/2309.17167.pdf">Paper</a>]
[<a href="https://aka.ms/dyval">Github</a>]
</p>

<details>
<summary>Abstract</summary>
Large language models (LLMs) have achieved remarkable performance in various evaluation benchmarks. However, concerns about their performance are raised on potential data contamination in their considerable volume of training corpus. Moreover, the static nature and fixed complexity of current benchmarks may inadequately gauge the advancing capabilities of LLMs. In this paper, we introduce DyVal, a novel, general, and flexible evaluation protocol for dynamic evaluation of LLMs. Based on our proposed dynamic evaluation framework, we build graph-informed DyVal by leveraging the structural advantage of directed acyclic graphs to dynamically generate evaluation samples with controllable complexities. DyVal generates challenging evaluation sets on reasoning tasks including mathematics, logical reasoning, and algorithm problems. We evaluate various LLMs ranging from Flan-T5-large to ChatGPT and GPT4. Experiments demonstrate that LLMs perform worse in DyVal-generated evaluation samples with different complexities, emphasizing the significance of dynamic evaluation. We also analyze the failure cases and results of different prompting methods. Moreover, DyVal-generated samples are not only evaluation sets, but also helpful data for fine-tuning to improve the performance of LLMs on existing benchmarks. We hope that DyVal can shed light on the future evaluation research of LLMs.

</details>

<p align="center">
<img src="/assets/img/dyval.jpg" style="width: 70%;"/>
</p>

- - -

## Meta Semantic Template for Evaluation of Large Language Models

*Added on: 03/10/2023.*

<p align="center">
  Yachuan Liu<sup>1</sup>,
  Liang Chen<sup>2</sup>,  
  Jindong Wang<sup>#3</sup>,  
  Qiaozhu Mei<sup>1</sup>,
  Xing Xie<sup>3</sup>
</p>  

<p align="center">
<sup>1</sup> University of Michigan,
<sup>2</sup> CUHK,
<sup>3</sup> Microsoft Research<br>
(#: Corresponding author)
</p>

<p align="center">
[<a href="https://arxiv.org/pdf/2310.01448.pdf">Paper</a>]
[<a href="https://aka.ms/promptbench">Github</a>]
</p>

<details>
<summary>Abstract</summary>
Do large language models (LLMs) genuinely understand the semantics of the language, or just memorize the training data? The recent concern on potential data contamination of LLMs has raised awareness of the community to conduct research on LLMs evaluation. In this paper, we propose MSTemp, an approach that creates meta semantic templates to evaluate the semantic understanding ability of LLMs. The core of MSTemp is not to perform evaluation directly on existing benchmark datasets, but to generate new out-of-distribution (OOD) evaluation sets using existing datasets as seeds. Specifically, for a given sentence, MSTemp leverages another language model to generate new samples while preserving its semantics. The new samples are called semantic templates to the original sentence. Then, MSTemp generates evaluation samples via sentence parsing and random word replacement on the semantic templates. MSTemp is highly flexible, dynamic, and cost-effective. Our initial experiments show that MSTemp-generated samples can significantly reduce the performance of LLMs using existing datasets as seeds. We hope this initial work can shed light on future research of LLMs evaluation.

</details>

<p align="center">
<img src="/assets/img/mstemp.jpg" style="width: 70%;"/>
</p>

- - -

## A survey on evaluation of large language models
 
<p align="center">
  Yupeng Chang<sup>*1</sup>,
  Xu Wang<sup>*1</sup>,  
  Jindong Wang<sup>#2</sup>,  
  Yuan Wu<sup>#1</sup>,  
  Kaijie Zhu<sup>3</sup>, 
  Hao Chen<sup>4</sup>,  
  Linyi Yang<sup>5</sup>, 
  Xiaoyuan Yi<sup>2</sup>, 
  Cunxiang Wang<sup>5</sup>,
  Yidong Wang<sup>6</sup>,
  Wei Ye<sup>6</sup>,
  Yue Zhang<sup>5</sup>,
  Yi Chang<sup>1</sup>,
  Philip S. Yu<sup>7</sup>,
  Qiang Yang<sup>8</sup>, 
  Xing Xie<sup>2</sup>
</p>  

<p align="center">
<sup>1</sup> Jilin University,
<sup>2</sup> Microsoft Research,
<sup>3</sup> Institute of Automation, CAS
<sup>4</sup> Carnegie Mellon University,
<sup>5</sup> Westlake University,
<sup>6</sup> Peking University,
<sup>7</sup> University of Illinois,
<sup>8</sup> Hong Kong University of Science and Technology<br>
(*: Co-first authors, #: Co-corresponding authors)
</p>

<p align="center">
[<a href="https://arxiv.org/abs/2307.03109">Paper</a>]
[<a href="https://github.com/MLGroupJLU/LLM-eval-survey">Github</a>]
</p>

<details>
<summary>Abstract</summary>
Large language models (LLMs) are gaining increasing popularity in both academia and industry, owing to their unprecedented performance in various applications. As LLMs continue to play a vital role in both research and daily use, their evaluation becomes increasingly critical, not only at the task level, but also at the society level for better understanding of their potential risks. Over the past years, significant efforts have been made to examine LLMs from various perspectives. This paper presents a comprehensive review of these evaluation methods for LLMs, focusing on three key dimensions: what to evaluate, where to evaluate, and how to evaluate. Firstly, we provide an overview from the perspective of evaluation tasks, encompassing general natural language processing tasks, reasoning, medical usage, ethics, educations, natural and social sciences, agent applications, and other areas. Secondly, we answer the `where' and `how' questions by diving into the evaluation methods and benchmarks, which serve as crucial components in assessing performance of LLMs. Then, we summarize the success and failure cases of LLMs in different tasks. Finally, we shed light on several future challenges that lie ahead in LLMs evaluation. Our aim is to offer invaluable insights to researchers in the realm of LLMs evaluation, thereby aiding the development of more proficient LLMs. Our key point is that evaluation should be treated as an essential discipline to better assist the development of LLMs. We consistently maintain the related open-source materials.

</details>

<p align="center">
<img src="https://github.com/MLGroupJLU/LLM-eval-survey/blob/main/imgs/framework.png?raw=true" style="width: 70%;"/>
</p>

- - -

## PromptBench: towards evaluating the adversarial robustness to prompts of LLMs

<p align="center">
  Kaijie Zhu<sup>1</sup>,
  Jindong Wang<sup>#2</sup>,  
  Jiaheng Zhou<sup>1</sup>,  
  Zichen Wang<sup>1</sup>,  
  Hao Chen<sup>3</sup>, 
  Yidong Wang<sup>4</sup>,  
  Linyi Yang<sup>5</sup>, 
  Wei Ye<sup>4</sup>, 
  Neil Zhenqiang Gong<sup>6</sup>,
  Yue Zhang<sup>5</sup>,
  Xing Xie<sup>2</sup>
</p>  

<p align="center">
<sup>1</sup> Institute of Automation, CAS,
<sup>2</sup> Microsoft Research,
<sup>3</sup> Carnegie Mellon University,
<sup>4</sup> Peking University,
<sup>5</sup> Westlake University,
<sup>6</sup> Duke University<br>
(#: Corresponding author)
</p>

<p align="center">

[<a href="https://arxiv.org/abs/2306.04528">Paper</a>]
[<a href="https://github.com/microsoft/promptbench">Github</a>]
[<a href="https://huggingface.co/spaces/March07/PromptBench">Demo</a>]
[<a href="https://www.bilibili.com/video/BV17X4y1W74A/">Video</a>]
[<a href="https://zhuanlan.zhihu.com/p/637219127">Blog</a>]
</p>

<details>
<summary>Abstract</summary>
The increasing reliance on Large Language Models (LLMs) across academia and industry necessitates a comprehensive understanding of their robustness to prompts. In response to this vital need, we introduce PromptBench, a robustness benchmark designed to measure LLMs' resilience to adversarial prompts. This study uses a plethora of adversarial textual attacks targeting prompts across multiple levels: character, word, sentence, and semantic. These prompts are then employed in diverse tasks, such as sentiment analysis, natural language inference, reading comprehension, machine translation, and math problem-solving. Our study generates 4,032 adversarial prompts, meticulously evaluated over 8 tasks and 13 datasets, with 567,084 test samples in total. Our findings demonstrate that contemporary LLMs are vulnerable to adversarial prompts. Furthermore, we present comprehensive analysis to understand the mystery behind prompt robustness and its transferability. We then offer insightful robustness analysis and pragmatic recommendations for prompt composition, beneficial to both researchers and everyday users. We make our code, prompts, and methodologies to generate adversarial prompts publicly accessible, thereby enabling and encouraging collaborative exploration in this pivotal field.

</details>


<p align="center">
<img src="/assets/img/promptbench.png" style="width: 70%;"/>
</p>

- - -

## GLUE-X: Evaluation from an Out-of-distribution Generalization Perspective

*This work is published at **ACL 2023** findings.*

<p align="center">
  Linyi Yang<sup>1</sup>,  
  Shuibai Zhang<sup>1,3</sup>,  
  Libo Qin<sup>2</sup>,  
  Yafu Li<sup>1</sup>, 
  Yidong Wang<sup>1</sup>,  
  Hanmeng Liu<sup>1</sup>, 
  Jindong Wang<sup>4</sup>, 
  Xing Xie<sup>4</sup>,
  Yue Zhang<sup>1</sup>
</p>  

<p align="center">
<sup>1</sup> Westlake University
<sup>2</sup> Central South University,
<sup>3</sup> University of Electronic Science and Technology of China,
<sup>4</sup> Microsoft Research<br>
</p>

<p align="center">
[<a href="https://arxiv.org/abs/2211.08073">Paper</a>]
[<a href="https://github.com/YangLinyi/GLUE-X">Github</a>]
[<a href="https://gluexbenchmark.com/">Leaderboard</a>]
[<a href="https://zhuanlan.zhihu.com/p/641488976">Blog</a>]
</p>

<details>
<summary>Abstract</summary>
Pre-trained language models (PLMs) are known to improve the generalization performance of natural language understanding models by leveraging large amounts of data during the pre-training phase. However, the out-of-distribution (OOD) generalization problem remains a challenge in many NLP tasks, limiting the real-world deployment of these methods. This paper presents the first attempt at creating a unified benchmark named GLUE-X for evaluating OOD robustness in NLP models, highlighting the importance of OOD robustness and providing insights on how to measure the robustness of a model and how to improve it. The benchmark includes 13 publicly available datasets for OOD testing, and evaluations are conducted on 8 classic NLP tasks over 21 popularly used PLMs, including GPT-3 and GPT-3.5. Our findings confirm the need for improved OOD accuracy in NLP tasks, as significant performance degradation was observed in all settings compared to in-distribution (ID) accuracy.

</details>

<p align="center">
<img src="/assets/img/glue-x.png" style="width: 50%;"/>
</p>

- - -

## PandaLM: An Automatic Evaluation Benchmark for LLM Instruction Tuning Optimization

<p align="center">
  Yidong Wang<sup>1,2*</sup>,
  Zhuohao Yu<sup>1*</sup>,  
  Zhengran Zeng<sup>1</sup>,  
  Linyi Yang<sup>2</sup>,  
  Cunxiang Wang<sup>2</sup>, 
  Hao Chen<sup>3</sup>,  
  Chaoya Jiang<sup>1</sup>, 
  Rui Xie<sup>1</sup>, 
  Jindong Wang<sup>3</sup>,
  Xing Xie<sup>3</sup>,
  Wei Ye<sup>1</sup>
  Shikun Zhang<sup>1</sup>
  Yue Zhang<sup>2</sup>
</p>  

<p align="center">
<sup>1</sup> Peking University,
<sup>2</sup> Westlake University,
<sup>3</sup> Microsoft Research<br>
</p>

<p align="center">
[<a href="https://arxiv.org/abs/2306.05087">Paper</a>]
[<a href="https://github.com/WeOpenML/PandaLM">Github</a>]
[<a href="https://huggingface.co/WeOpenML/PandaLM-7B-v1">Model</a>]
[<a href="https://zhuanlan.zhihu.com/p/626391857">Blog</a>]
</p>

<details>
<summary>Abstract</summary>
Instruction tuning large language models (LLMs) remains a challenging task, owing to the complexity of hyperparameter selection and the difficulty involved in evaluating the tuned models. To determine the optimal hyperparameters, an automatic, robust, and reliable evaluation benchmark is essential. However, establishing such a benchmark is not a trivial task due to the challenges associated with evaluation accuracy and privacy protection. In response to these challenges, we introduce a judge large language model, named PandaLM, which is trained to distinguish the superior model given several LLMs. PandaLM's focus extends beyond just the objective correctness of responses, which is the main focus of traditional evaluation datasets. It addresses vital subjective factors such as relative conciseness, clarity, adherence to instructions, comprehensiveness, and formality. To ensure the reliability of PandaLM, we collect a diverse human-annotated test dataset, where all contexts are generated by humans and labels are aligned with human preferences. Our results indicate that PandaLM-7B achieves 93.75% of GPT-3.5's evaluation ability and 88.28% of GPT-4's in terms of F1-score on our test dataset. PandaLM enables the evaluation of LLM to be fairer but with less cost, evidenced by significant improvements achieved by models tuned through PandaLM compared to their counterparts trained with default Alpaca's hyperparameters. In addition, PandaLM does not depend on API-based evaluations, thus avoiding potential data leakage. 
</details>

<p align="center">
<img src="https://github.com/WeOpenML/PandaLM/raw/main/figures/main-figure.png" style="width: 70%;"/>
</p>

- - -

## On the robustness of ChatGPT: an adversarial and OOD perspective

*This work is published at ICLR 2023 workshop on [Trustworthy and Reliable Large-Scale Machine Learning Models](https://rtml-iclr2023.github.io/) and is recognized as the **highlighted** paper.*

<p align="center">
  Jindong Wang<sup>1</sup>,  
  Xixu Hu<sup>2</sup>,  
  Wenxin Hou<sup>3</sup>,  
  Hao Chen<sup>4</sup>, 
  Runkai Zheng<sup>5</sup>,  
  Yidong Wang<sup>6</sup>, 
  Linyi Yang<sup>7</sup>, 
  Haojun Huang<sup>3</sup>,
  Wei Ye<sup>6</sup>,
  Xiubo Geng<sup>3</sup>,
  Binxin Jiao<sup>3</sup>,
  Yue Zhang<sup>7</sup>,
  Xing Xie<sup>1</sup>
</p>  

<p align="center">
<sup>1</sup> Microsoft Research
<sup>2</sup> City University of Hong Kong,
<sup>3</sup> Microsoft STCA,
<sup>4</sup> Carnegie Mellon University,
<sup>5</sup> Chinese University of Hong Kong (Shenzhen),
<sup>6</sup> Peking University,
<sup>7</sup> Westlake University<br>
</p>

<p align="center">
[<a href="https://arxiv.org/abs/2302.12095">Paper</a>]
[<a href="https://github.com/microsoft/robustlearn">Github</a>]
[<a href="https://zhuanlan.zhihu.com/p/612391048">Blog</a>]
</p>

<details>
<summary>Abstract</summary>
ChatGPT is a recent chatbot service released by OpenAI and is receiving increasing attention over the past few months. While evaluations of various aspects of ChatGPT have been done, its robustness, i.e., the performance to unexpected inputs, is still unclear to the public. Robustness is of particular concern in responsible AI, especially for safety-critical applications. In this paper, we conduct a thorough evaluation of the robustness of ChatGPT from the adversarial and out-of-distribution (OOD) perspective. To do so, we employ the AdvGLUE and ANLI benchmarks to assess adversarial robustness and the Flipkart review and DDXPlus medical diagnosis datasets for OOD evaluation. We select several popular foundation models as baselines. Results show that ChatGPT shows consistent advantages on most adversarial and OOD classification and translation tasks. However, the absolute performance is far from perfection, which suggests that adversarial and OOD robustness remains a significant threat to foundation models. Moreover, ChatGPT shows astounding performance in understanding dialogue-related texts and we find that it tends to provide informal suggestions for medical tasks instead of definitive answers. Finally, we present in-depth discussions of possible research directions.

</details>

<p align="center">
<img src="https://github.com/microsoft/robustlearn/raw/main/chatgpt-robust/fig-robchat.png" style="width: 70%;"/>
</p>

