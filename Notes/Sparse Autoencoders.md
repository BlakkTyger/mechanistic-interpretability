# Sparse Autoencoders

Question: Why are intermediate activations of LLMs not interpretable?
Answer: **Superposition -** single neuron can encode multiple concepts simultaneously

- **Autoencoder** 
	- neural network that learns to compress and decompress its input
	- goal of the model is to minimize the difference between the input vector and the reconstructed output
	- Eg: Input: 100 neurons, Intermediate layer: 50 neurons, Output Layer: 100 neurons
	- Intermediate layer can also have a higher activation, in order to untangle superpositions of features: Input: 50 neurons, Intermediate layer: 100 neurons, Output Layer: 50 neurons. This is what is used in SAEs for LLM interpretability.
	
- **Sparse Autoencoder: High Level Idea**
	- Weak dictionary learning algorithm
	- 
	- Sparsity: activate only a small proportion of neurons in the intermediate layers (not-dense)
	- SAEs have sparsity penalty in their loss function
	- intermediate vectors / intermediate activations created by the SAEs are sparse, which means that they have as many zero values as possible
	- Training Input: intermediate activations of LLMs at various points in their architecture, often between two layers. 
	- A given SAE is trained on the activations between two layers, eg: the activations between layer 11 and 12 because we want to understand what it means when a given neuron of a given activation is activated.
	- Each component of these activations, extracted through the training of an SAE, is called a **feature**

- **Detailed procedure of extracting features**
	- Architecture
		1. ReLU upsampling layer
		2. Linear downsampling layer
	- Training Pipeline
		1. **Sparsity and Concept Reduction:** Sparsity is ensured by the L1 norm in the Cost Function. This ensures that although representation may have high dimensionality, only a small fraction of neurons are activated
		2. 
	- Inference Pipeline
		1. **Encoding Intermediate Activations:** activations -> sparse high-dimensional representations 
		2. Lmao