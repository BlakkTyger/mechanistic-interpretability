# mechanistic-interpretability
Exporing Mechansitic Interpretability and LLM Internals research for SURGE 2025

Test

## Recurring Links
- [Presentation](docs.google.com/presentation/d/1qldFeePw9EnhpDPRC5mtWezARGq-AyVLrA-ChrUdpqU/edit?slide=id.g3327e10295c_0_1100#slide=id.g3327e10295c_0_1100)
- [Document](https://docs.google.com/document/d/1THCdHUTvAYaAXqn1j9ZKqB0FiLh09a8BKhOV6_n76tc/edit?tab=t.0)

## Work
- [x] [Many-shot Jailbreaking Paper](https://www-cdn.anthropic.com/af5633c94ed2beb282f6a53c595eb437e8e7b630/Many_Shot_Jailbreaking__2024_04_02_0936.pdf#cite.wei2023jailbreak): Notes
- [x] [Function Vectors Paper](https://arxiv.org/pdf/2310.15213)
  - [x] Read and Notes
  - [x] Implementation
- [ ] SSR Paper
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

### Sparse AutoEncoders


### LLM Safety and Alignment
1. [Foundational Challenges in Assuring Alignment and Safety of Large Language Models](https://arxiv.org/pdf/2404.09932)
2. 
### Adversarial Attacks on LLMs
1. [Are aligned neural networks adversarially aligned?](https://arxiv.org/pdf/2203.07281)
2. https://lilianweng.github.io/posts/2023-10-25-adv-attack-llm/
3. Black Box Attacks: https://arxiv.org/abs/2307.02483
4. White Box Adversarial Suffix Attack, Greedy Coordinate Gradient ascent: https://arxiv.org/abs/2307.15043
5. [Mitigating Adversarial Attacks in LLMs through Defensive Suffix Generation](arxiv.org/html/2412.13705)

### Interpretability of Jailbreak
[GPT-DeepResearch](https://chatgpt.com/share/684eac7f-69ac-8002-a93a-9b766e2f12c2)
[Circuit Tracing on Jailbreaks](https://transformer-circuits.pub/2025/april-update/index.html)

1. [Using MI to Craft Adversarial Attacks against LLMs](https://arxiv.org/pdf/2503.06269)
2. [ASETF: A Novel Method for Jailbreak Attack on LLMs through Translate Suffix Embeddings](https://arxiv.org/pdf/2402.16006)
3. [JailbreakLens](https://arxiv.org/pdf/2411.11114v1)
4. [GRAPH OF ATTACKS: IMPROVED BLACK-BOX AND INTERPRETABLE JAILBREAKS FOR LLMS](https://arxiv.org/pdf/2504.19019)
5. [Towards Understanding Jailbreak Attacks in LLMs: A Representation Space Analysis](https://arxiv.org/pdf/2406.10794): propose that successful jailbreaks shift harmful prompts into clusters typically occupied by harmless ones
6. [UNDERSTANDING JAILBREAK SUCCESS: A STUDY OF LATENT SPACE DYNAMICS IN LARGE LANGUAGE MODELS](https://arxiv.org/pdf/2406.09289): examine similarities in activation vectors across different jailbreak attacks, suggesting that these commonalities reflect shared internal mechanisms for bypassing safety measure
7. [Explain LLM Safety through Intermediate Hidden States](https://arxiv.org/pdf/2406.05644): jailbreaks disrupt the association between harmfulness and negative emotion learned via safety alignment
8. [SAFETY LAYERS IN ALIGNED LARGE LANGUAGE MODELS](https://arxiv.org/pdf/2408.17003): identify that representations from middle layers of the model are crucial for distinguishing malicious queries from safe ones.
9. [Causality analysis for evaluating the security of large language models](https://arxiv.org/pdf/2312.07876)
	- analyzes the safety mechanism within LLMs at the level of circuit, particularly, the neurons in MLP layers
	- find a special neuron that changing the value of that neuron to 0 could impact the safe output of the model completely
10. [Finding Safety Neurons in Large Language Models](https://arxiv.org/pdf/2406.14144): propose activation contrasting to locate key neurons that are responsible for safety behaviors and dynamic activation patching to evaluate their causal effects

### Sparse Coders
1. [Sparse Crosscoders](https://transformer-circuits.pub/2024/crosscoders/index.html)
2. [Robustly identifying concepts introduced during chat fine-tuning using crosscoders](https://arxiv.org/pdf/2504.02922v1)
	1. [GPT-explain](https://chatgpt.com/share/6850161b-f984-8002-81e3-5993cd7c672b)

### LLM Architectures and Training
1. [Language Models are Unsupervised Multitask Learners](https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)
2. [Language Models are Few-Shot Learners](https://arxiv.org/pdf/2005.14165)

### In-Context Learning
1. [Label Words are Anchors: An Information Flow Perspective for Understanding In-Context Learning](https://arxiv.org/pdf/2305.14160)
2. [Noisy Channel Language Model Prompting for Few-Shot Text Classification](https://aclanthology.org/2022.acl-long.365.pdf)
3. [Chain-of-Thought Prompting Elicits Reasoning in Large Language Models](https://arxiv.org/pdf/2201.11903)
4. [An Explanation of In-context Learning as Implicit Bayesian Inference](https://arxiv.org/pdf/2111.02080)
5. [The Mystery of In-Context Learning: A Comprehensive Survey on Interpretation and Analysis](https://arxiv.org/pdf/2311.00237v3)

### ICL Interpretability
Similar: Steering Vectors, In Context Vectors, Task Vectors, Function Vectors
- [Steering Vectors Video](https://www.youtube.com/watch?v=cp-YSyc5aW8)

1. [Function Vectors in LLMs](https://arxiv.org/pdf/2310.15213)
2. [In-context learning creates task vectors](https://arxiv.org/pdf/2310.15916)
3. [RAVEL: Evaluating Interpretability Methods on Disentangling Language Model Representations](https://arxiv.org/pdf/2402.17700)
	- When choosing intervention sites, we limit our search to the residual stream above the last entity token. However, representations of attributes can be distributed across multiple tokens or layers. We encourage future work to explore different intervention sites when using this benchmark.
4. [Learnable In-Context Vector for Visual Question Answering](https://proceedings.neurips.cc/paper_files/paper/2024/file/12d3e63be5574088f7c1bbc9162060bf-Paper-Conference.pdf)
5. [ICVs: Making In Context Learning More Effective and Controllable Through Latent Space Steering](https://arxiv.org/pdf/2311.06668)
6. [Contextualize-then-Aggregate: Circuits for In-Context Learning in Gemma-2 2B](https://arxiv.org/pdf/2504.00132v1)
7. 

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

### Research Ideas
1. Input Prompt compression (or, token optimization): [Evil Twins Paper](https://aclanthology.org/2024.emnlp-main.4.pdf)
2. Improvements upon SubSpace Rerouting: 
	- [GPT Response](https://chatgpt.com/share/6850431d-7594-8002-ad94-63364627563d)
	- [Repo](https://github.com/Sckathach/subspace-rerouting/blob/main/TODO.md)
	- 
