Main Paper [Contextualize-then-Aggregate: Circuits for In-Context Learning in Gemma-2 2B](https://arxiv.org/pdf/2504.00132v1)
Paper References for ICL Interpretability:
1. [Rethinking the Role of Demonstrations: What Makes In-Context Learning Work?](https://arxiv.org/pdf/2202.12837)
2. [What Can Transformers Learn In-Context? A Case Study of Simple Function Classes](https://arxiv.org/pdf/2208.01066)
3. [What learning algorithm is in-context learning? Investigations with linear models](https://arxiv.org/pdf/2211.15661)
4. [An Information Flow Perspective for Understanding In-Context Learning](https://aclanthology.org/2023.emnlp-main.609.pdf)
5. [Function Vectors in LLMs](https://openreview.net/pdf?id=AwyxtyMwaG)
6. [In-Context Learning Creates Task Vectors](https://arxiv.org/pdf/2310.15916)
7. [SCALING SPARSE AUTOENCODER CIRCUITS FOR IN-CONTEXT LEARNING](https://openreview.net/pdf?id=Pa1vr1Prww)
8. [Language Models are Few-Shot Learners](https://arxiv.org/pdf/2005.14165)


**Function Vectors:** attention heads whose output encodes task information, and which are causally responsible for the prediction of the response

**Problem:** However, the circuit by which these vectors are assembled remains only
partly understood

**Proposition in recent work:** each fewshot example’s output token computes task information, which is then aggregated by attention heads to predict the next output
1. [An Information Flow Perspective for Understanding In-Context Learning](https://aclanthology.org/2023.emnlp-main.609.pdf)
2. [REVISITING IN-CONTEXT LEARNING INFERENCE CIRCUIT IN LARGE LANGUAGE MODELS](https://openreview.net/pdf?id=xizpnYNvQq)
3. [SCALING SPARSE AUTOENCODER CIRCUITS FOR IN-CONTEXT LEARNING](https://openreview.net/pdf?id=Pa1vr1Prww)

**Problem with new propositions:** this strategy has also been observed to leave part of the models’ performance unexplained
1. [REVISITING IN-CONTEXT LEARNING INFERENCE CIRCUIT IN LARGE LANGUAGE MODELS](https://openreview.net/pdf?id=xizpnYNvQq)

Mechanistic Interpetability Methods Used: Causal Interventions:
1. [Investigating Gender Bias in Language Models Using Causal Mediation Analysis](https://proceedings.neurips.cc/paper/2020/file/92650b2e92217715fe312e6fa7b90d82-Paper.pdf)
2. [Locating and Editing Factual Associations in GPT](https://arxiv.org/pdf/2202.05262)
3. [Causal Abstractions of Neural Networks](https://arxiv.org/pdf/2106.02997)

to identify a circuit performing ICL on five naturalistic tasks (Capitalization, Country-Capital,
Present-Past, Person-Sport, Copying) in Gemma-2 2B

---

Novel Contributions:
1. Obtain causally faithful information flow from the fewshot examples to the next-token prediction, explaining ≥ 90% of the model’s performance.
2. Establish the importance and function of a contextualization step that precedes aggregation

---

Limitations:
1. Focuses on causal understanding of information flow between positions, and does not interpret MLPs or individual heads. 
2. 


Future Work:
1. Combine our results with a further scaled-up version of the sparse feature circuits to understand the contextualization step at the level of individual representations

---

