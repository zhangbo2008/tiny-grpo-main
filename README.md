train.py :255
#======整体把握训练流程. # 遍历每一个提示词.也就是问答对,锁参数跑actor和ref模型的结果,记录到expericence. 这是acotr跑的是pi_theta_old, ref跑的是pi_ref
                          #然后训练时候actor再跑一遍, 这时候跑的就是pi_theta.之后套r1论文(1)即可.
                          

















# Minimal GRPO implementation

Goal: Working toy implementation of llama-3.2-3b locally RL training with GRPO. Understanding the algorithm & hyper parameters. Just running everything locally on a single node.

### Setup

1. Create conda env

```
conda create --name grpo python=3.12 -y
conda activate grpo
```

2. Install dependencies

```
pip install -r requirements.txt
pip install flash-attn --no-build-isolation
```

3. Play with the source in `train.py`

```
python train.py
```

### Inspiration

- [OpenRLHF](https://github.com/OpenRLHF/OpenRLHF)
- [Spinning Up in Deep RL](https://spinningup.openai.com/en/latest/)


### References

- [DeepSeek-R1 tech report](https://github.com/deepseek-ai/DeepSeek-R1/blob/main/DeepSeek_R1.pdf)
- [DeepSeekMath: Pushing the Limits of Mathematical Reasoning in Open Language Models](https://arxiv.org/abs/2402.03300)
"# tiny-grpo-main" 
