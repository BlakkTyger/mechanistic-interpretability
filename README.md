# mechanistic-interpretability
Exporing Mechansitic Interpretability and LLM Internals research for SURGE 2025

## Recurring Links
- [Presentation](docs.google.com/presentation/d/1qldFeePw9EnhpDPRC5mtWezARGq-AyVLrA-ChrUdpqU/edit?slide=id.g3327e10295c_0_1100#slide=id.g3327e10295c_0_1100)
- [Document](https://docs.google.com/document/d/1THCdHUTvAYaAXqn1j9ZKqB0FiLh09a8BKhOV6_n76tc/edit?tab=t.0)

## Work
- [x] [Many-shot Jailbreaking Paper](https://www-cdn.anthropic.com/af5633c94ed2beb282f6a53c595eb437e8e7b630/Many_Shot_Jailbreaking__2024_04_02_0936.pdf#cite.wei2023jailbreak): Notes
- [ ] [Function Vectors Paper](https://arxiv.org/pdf/2310.15213)
  - [ ] Read and Notes
  - [ ] Implementation
- [ ] [GPT-RE Paper](https://arxiv.org/pdf/2305.02105): Notes
- [ ] [NNSight](https://nnsight.net/): Understand and go through docs
- [ ] Interpretability Video by David Bau
  - [ ] [Video](https://www.youtube.com/watch?v=8QPVKpzyZdY&ab_channel=UCBerkeleyEECS)
  - [ ] [Presentation](https://rdi.berkeley.edu/understanding_llms/assets/jan30.pdf) 

## Resources

[Jailbreak Repo](https://github.com/elder-plinius/L1B3RT4S)
[ChatGPT-DeepResearch-PapersSummary](https://chatgpt.com/c/68491b74-7164-8002-b4b2-9ecd68ff465e)


### Getting Started with Mechanistic Interpretability

[Open Problems in Mechanistic Interpretability](https://arxiv.org/pdf/2501.16496): Gold Standard
[200 Concrete Open Problems in Mechanistic Interpretability](https://www.alignmentforum.org/s/yivyHaCAmMJ3CqSyj)
### Adversarial Attacks on LLMs

1. [Are aligned neural networks adversarially aligned?](https://arxiv.org/pdf/2203.07281)
2. https://lilianweng.github.io/posts/2023-10-25-adv-attack-llm/
3. Black Box Attacks: https://arxiv.org/abs/2307.02483
4. White Box Adversarial Suffix Attack, Greedy Coordinate Gradient ascent: https://arxiv.org/abs/2307.15043

### LLM Architectures and Training
1. [Language Models are Unsupervised Multitask Learners](https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)
2. [Language Models are Few-Shot Learners](https://arxiv.org/pdf/2005.14165)

### In-Context Learning
1. [Label Words are Anchors: An Information Flow Perspective for Understanding In-Context Learning](https://arxiv.org/pdf/2305.14160)
2. [Noisy Channel Language Model Prompting for Few-Shot Text Classification](https://aclanthology.org/2022.acl-long.365.pdf)
3. [Chain-of-Thought Prompting Elicits Reasoning in Large Language Models](https://arxiv.org/pdf/2201.11903)
4. [An Explanation of In-context Learning as Implicit Bayesian Inference](https://arxiv.org/pdf/2111.02080)
5. [The Mystery of In-Context Learning: A Comprehensive Survey on Interpretation and Analysis](https://arxiv.org/pdf/2311.00237v3)
   


### GCG-Optimizations
1. GCG For Adversarial Suffix Crafting:
	1. [Universal and Transferable Adversarial Attacks on Aligned Language Models](https://arxiv.org/pdf/2307.15043v2): Paper in which GCG was introduced
	2. [AUTOPROMPT](https://arxiv.org/pdf/2010.15980): Gradient Based Optimization of tokens was inspired from this
	3. [Optimization via Probe Sampling](https://arxiv.org/pdf/2403.01251)
	4. [i-DeGCG](https://arxiv.org/pdf/2408.14866)
	5. [MAGIC (Index Gradients)](https://arxiv.org/pdf/2412.08615)
	6. [I-GCG](https://arxiv.org/pdf/2405.21018)
	7. [Momentum](https://arxiv.org/pdf/2405.01229)
2. Greedy Coordinate Descent General Optimizations:
	1. [Nearest Neighbor based Greedy Coordinate Descent](https://proceedings.neurips.cc/paper_files/paper/2011/file/160c88652d47d0be60bfbfed25111412-Paper.pdf)
	2. [Greedy 2-Coordinate Updates for Optimizing with an Equality Constraint](https://openreview.net/pdf?id=v0vaaGQC3GR)
	3. [Accelerated Stochastic Greedy Coordinate Descent by Soft Thresholding Projection onto Simplex](https://proceedings.neurips.cc/paper_files/paper/2017/file/84b20b1f5a0d103f5710bb67a043cd78-Paper.pdf)
3. Discrete Optimization Techniques for LLM Tokens:
	1. [GlitchMiner: Mining Glitch Tokens in Large Language Models via Gradient-based Discrete Optimization](https://arxiv.org/pdf/2410.15052)
	2. [RLPrompt](arxiv.org/pdf/2205.12548)
	3. [learning the target distribution with a continuous matrix of coefficients](https://arxiv.org/pdf/2104.13733)
	4. [Langevin Dynamics based optimization](https://arxiv.org/pdf/2205.12558)
	5. [FluentPrompt based on Langevin Dynamics](https://arxiv.org/pdf/2212.10539)
	6. [GRIPS (edit-based search approach)](https://arxiv.org/pdf/2203.07281)