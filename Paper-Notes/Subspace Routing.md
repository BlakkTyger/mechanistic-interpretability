# Using Mechanistic Interpretability to Craft Adversarial Attacks against LLMs

[Paper Link](https://arxiv.org/pdf/2503.06269)
[GitHub repo link](https://github.com/Sckathach/subspace-rerouting)

**Acceptance subspaces** - sets of feature vectors that do not trigger the model’s refusal mechanisms

Steps for the algorithm:
1. Identify Acceptance Subspaces (HOW?)
2. Use gradient-based optimization to reroute embeddings from refusal subspaces to acceptance subspaces (Better Optimization?)


Metadata about the algorithm:
1. Models used: Gemma2, Llama3.2, and Qwen2.5

### Identification of Subspaces

#### Refusal Subspaces

##### Papers:
1. [Refusal in Language Models Is Mediated by a Single Direction](https://arxiv.org/pdf/2406.11717)
	- found that effective jailbreak suffixes can selectively interfere with these safety-relevant heads.
	- refusal subspaces could also be defined using a single direction. This direction, called the refusal direction represented by a unit vector of dimension d (that is the embedding direction), is computed by taking the difference in mean between the harmful activations and the harmless ones
2. [Understanding Jailbreak Success: A Study of Latent Space Dynamics in Large Language Models](https://arxiv.org/pdf/2406.09289)
3. [JailbreakLens: Interpreting Jailbreak Mechanism in the Lens of Representation and Circuit](https://arxiv.org/pdf/2411.11114v1)
4. [On the Role of Attention Heads in Large Language Model Safety](https://arxiv.org/pdf/2410.13708): 
	- demonstrated that only a small subset of attention heads are responsible for implementing safety mechanisms
	- ablating the head with the largest score was sufficient to drastically reduce the model’s ability to refuse
		- SSR Contradicts: targeting the group of 3-4 highest-scoring heads was necessary to achieve reasonable attack success rate

##### Method
1. Run inference on contrastive dataset D which contains pairs of bad and good prompts
2. Extracting the last token’s activations at each layer during this inference
3. Implement Principal Component Analysis of sentence representations from D to observe the progression of clustering

![[Pasted image 20250617132039.png]]

4. Implement linear probes - single-layer neural networks mapping activations to binary harmful-harmless classification.
	- probes achieve over 95% accuracy as early as the third layer of the model
	- harmful and harmless content occupies linearly separable regions in activation space at early processing stages

Interpretability Method:
1. Direct Logit Attribution: DLA performed on layers maps the outputs of each layer to logit space, and quantifies their contribution to the final token prediction by computing the logit difference between refusal and acceptance tokens.  A large value for a specific component means the direct contribution of this component to the next token is important. Thus, we can choose to only target the layer with the largest logit difference.
2. Activation Patching: 


##### Papers on Interpretability methods used
1. [Locating and Editing Factual Associations in GPT](https://arxiv.org/pdf/2202.05262)
2. [Interpretability in the Wild](https://arxiv.org/pdf/2211.00593)
3. [Towards Automated Circuit Discovery for Mechanistic Interpretability](https://arxiv.org/pdf/2304.14997)

### Relevant Papers
1. [Steering Llama 2 via Contrastive Activation Addition](https://arxiv.org/pdf/2312.06681)
2. 


SSR FOR ICL: https://chatgpt.com/share/6851b2d2-66c0-8002-bb58-3f08a49c4599