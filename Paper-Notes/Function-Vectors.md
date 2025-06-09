# FUNCTION VECTORS IN LARGE LANGUAGE MODELS

[Link](https://arxiv.org/pdf/2310.15213)

## Contributions of the paper
- reports the presence of a simple neural mechanism that represents an input-output function as a vector within autoregressive transformer language models
- It is found that a small number attention heads transport a compact representation of the demonstrated task, which we call a function vector (FV).
- Function Vectors often contain information that encodes the output space of the function, this information alone is not sufficient to reconstruct an FV
- Function Vectors to some extent can be summed to create vectors that trigger new complex tasks

## Keywords
- causal mediation analysis
- in context learning
- activation patching: to determine the presence of a handful of attention heads that mediate many ICL tasks.
- Word-embedding vector arithmetic (Mikolov et al., 2013; Levy & Goldberg, 2014; Merullo et al., 2023)
- 


FV can be formed by summing outputs of the causal attention heads.
