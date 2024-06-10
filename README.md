
# agent-finetuing
finetune open source llama2






### update
- [24/6/10] open code







## guidelines

#### environment
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

#### support model
- LLaMA
- LLaMA2

#### train technology
- LoRA


### How to run
```
cd ./script/sft
bash run_sft.sh
```
