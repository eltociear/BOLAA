# Introduction
This is the repo for [BOLAA paper](https://arxiv.org/abs/2308.05960). 
Note this is an initial release (may be a little bit messy) of our repo in response of many requests. We will keep cleaning and updating! 

## Installation
1. Setup the [fastchat](https://github.com/lm-sys/FastChat) to use local open-source LLMs. Go to next step if you only test openai API.
2. Setup OPENAI API KEY in both [webrun/config](./web_run/config.py) and [hotpotqa_run/config](./hotpotqa_run/config.py). Skip this if you only test open-source LLMs.  
2. Setup the [webshop enviroment](./webshop/) if you are testing web agent
3. Setup the agent_benchmarking environment as follows:
```
conda create -n agent_benchmark python=3.10 -y
conda activate agent_benchmark
pip install -r requirements.txt
```
## Web Agent Simulation
```
python run_webagent.py --agent_name Search_Click_Control_Webrun_Agent --llm_name gpt-3.5-turbo --max_context_len 4000
```
other agent options can be found in [test_webagent.sh](./test_webagent.sh)

## HotpotQA Agent Simulation
```
python run_hotpotqaagent.py --agent_name React_HotPotQA_run_Agent --llm_name gpt-3.5-turbo --max_context_len 4000
```
other agent options commands can be found in [test_hotpotqa.sh](./test_hotpotqa.sh)

## Citation
If you find our paper or code useful, please cite
```
@misc{liu2023bolaa,
      title={BOLAA: Benchmarking and Orchestrating LLM-augmented Autonomous Agents}, 
      author={Zhiwei Liu and Weiran Yao and Jianguo Zhang and Le Xue and Shelby Heinecke and Rithesh Murthy and Yihao Feng and Zeyuan Chen and Juan Carlos Niebles and Devansh Arpit and Ran Xu and Phil Mui and Huan Wang and Caiming Xiong and Silvio Savarese},
      year={2023},
      eprint={2308.05960},
      archivePrefix={arXiv},
      primaryClass={cs.AI}
}
```

## Acknowledge
- Part of our environment code reuse [ReAct](https://github.com/ysymyth/ReAct/tree/master) code. 
- Our LLM API is based on [Langchain](https://github.com/langchain-ai/langchain)
- We use the [WebShop](https://github.com/princeton-nlp/WebShop) and [HotPotQA](https://hotpotqa.github.io/) for testing.