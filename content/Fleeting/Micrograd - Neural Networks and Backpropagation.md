---
link: https://karpathy.ai/zero-to-hero.html
---
- AI models the brain as a bunch of neurons giving weighted inputs and the final decision is their collective input.
- Neuron's are actually pretty complex, we model them as having _weights_ and _biases_.

- While training, the model is given a bunch of inputs and a bunch of outputs.
- **Forward pass**: given input and weights (neurons), the NN computes the output.
- **Backpropagation:** now the model works backwards, calculating the gradient of each weight/neuron.
	- It's basically calculating how much each weight affects the output.
	- This is done using partial derivatives and chain rule!
	- We are essentially trying to calculate the rate of change of the output, w.r.t a particular weight.
	- Drawing the input-output graph helps us see how a particular value affects the output.
		- Each operation's _local gradient_ can be calculated like a regular derivative.
		- $\frac{dy}{dx} = \frac{dy}{dt}\frac{dt}{dx}$ Here $\frac{dy}{dt}$ is the local gradient.
		- With multiple layers,  the output of one neuron feeds into another neuron.
		- In such cases the gradient of the first (from the left) neuron is higher cuz it affects other neurons.
		- So we multiply it by the gradient of the following neuron.
		- This makes mathematical sense too via chain rule.

- Each neuron is modeled as a `Value` object.