
# Enhancing the General Agent Capabilities of Low-Parameter LLMs through Tuning and Multi-Branch Reasoning
<div align="center">

<div>
    <a href='' target='_blank'>Qinhao Zhou</a><sup>1</sup>&emsp;
    <a href='' target='_blank'>Zihan Zhang</a><sup>1</sup>&emsp;
    <a href='https://scholar.google.com.hk/citations?hl=zh-CN&user=-D5k5ioAAAAJ&view_op=list_works' target='_blank'>Xiang Xiang</a><sup>1</sup>&emsp;
    <a href='' target='_blank'>Ke Wang</a><sup>2</sup>&emsp;
    <a href='' target='_blank'>Yuchuan Wu</a><sup>2</sup>&emsp;
    <a href='' target='_blank'>Yongbin Li</a><sup>2</sup>
    
</div>
<div>
<sup>1</sup>School of Artificial Intelligence and Automation, Huazhong University of Science and Technology&emsp;

<sup>2</sup>Alibaba  Group&emsp;
</div>
</div>

The code repository for "[Enhancing the General Agent Capabilities of Low-Parameter LLMs]([https://github.com/HAIV-Lab/LLM-TMBR](https://aclanthology.org/2024.findings-naacl.184/)" in PyTorch.  If you use any content of this repo for your work, please cite the following bib entry: 

```
@inproceedings{zhou2024enhancing,
  title={Enhancing the General Agent Capabilities of Low-Parameter LLMs through Tuning and Multi-Branch Reasoning},
  author={Zhou, Qinhao and Zhang, Zihan and Xiang*, Xiang and Wang, Ke and Wu, Yuchuan and Li, Yongbin},
  booktitle={NAACL 2024 (Annual Conference of the North American Chapter of the Association for Computational Linguistics)},
  year={2024}
}
```



## update
- [24/6/10] open code

## Abstract
 Open-source pre-trained Large Language Models (LLMs) exhibit strong language understanding and generation capabilities, making them highly successful in a variety of tasks. 
 However, when used as agents for dealing with complex problems in the real world, their performance is far inferior to large commercial models such as ChatGPT and GPT-4. 
 As intelligent agents, LLMs need to have the capabilities of task planning, long-term memory, and the ability to leverage external tools to achieve satisfactory performance. 
 Various methods have been proposed to enhance the agent capabilities of LLMs. On the one hand, methods involve constructing agent-specific data and fine-tuning the models. 
 On the other hand, some methods focus on designing prompts that effectively activate the reasoning abilities of the LLMs. We explore both strategies on the 7B and 13B models. 
 We propose a comprehensive method for constructing agent-specific data using GPT-4. 
 Through supervised fine-tuning with constructed data, we find that for these models with a relatively small number of parameters, supervised fine-tuning can significantly reduce hallucination outputs and formatting errors in agent tasks. 
 Furthermore, techniques such as multi-path reasoning and task decomposition can effectively decrease problem complexity and enhance the performance of LLMs as agents. 
 We evaluate our method on five agent tasks of AgentBench and achieve satisfactory results. 
<p></p>

## Overall Process

<div align="center">
<img src="imgs/pip.png" width="93%">
</div>
<p></p>

<div>
We use GPT4 to generate agent data for sft. Besides, we employ backtracking and multi-branch reasoning techniques to optimize the performance of individual agent tasks.
</div>


## Results
<div>
The following table shows the main results of our proposed method.
</div>

<div align="center">
<img src="imgs/main_table.png" width="96%">
</div>

## environment
```
accelerate==0.21.0
datasets==2.13.1
scikit-learn==1.3.0
sentencepiece==0.1.99
tqdm==4.65.0
transformers==4.31.0
wandb==0.15.8
peft==0.4.0
torch==2.0.1
trl==0.5.0
deepspeed==0.10.0
```

## support model 
- LLaMA
- LLaMA2



## How to run
```
cd ./script/sft
bash run_sft.sh
```
## Acknowledge
This repo is based on [LLM-RLHF-Tuning](https://github.com/Joyce94/LLM-RLHF-Tuning).
