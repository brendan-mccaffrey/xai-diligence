# Technology Overview


### Attention: Huge Leap

In 2014, an Attention mechanism was introduced by Dzmitry Bahdanau, Kyunghyun Cho, and Yoshua Bengio. This became the foundation for the Transformer.
- [Neural Machine Translation by Jointly Learning to Align and Translate](https://arxiv.org/abs/1409.0473)
- [ffective Approaches to Attention-based Neural Machine Translation](https://arxiv.org/abs/1508.04025)

The attention mechanism allows the model to assign different weights or importance to different parts of the input sequence when making predictions or generating output. Instead of relying solely on fixed-length vector representations or encoding the entire input sequence into a fixed-length representation, the attention mechanism enables the model to dynamically attend to relevant parts of the input at each step of the computation.

In a typical attention mechanism, there are three main components:

1. Query: A query represents the current step or position in the output generation process. It is used to compare against different parts of the input sequence to determine their relevance.

2. Key: The keys are representations of the different parts of the input sequence. These keys are compared to the query to measure their similarity or relevance.

3. Value: The values are additional information associated with the input sequence parts. They provide the context or content that the model focuses on.

The attention mechanism computes a similarity score between the query and each key, which determines the relevance or attention assigned to the corresponding value. These similarity scores are typically computed using dot products, additive or multiplicative operations, or neural networks.

The resulting attention weights are used to weight the values associated with the input sequence parts. This weighted information is then combined or aggregated to provide a context-aware representation for the current step, allowing the model to focus more on relevant parts of the input.

By incorporating attention mechanisms into deep learning models, they can effectively capture dependencies between different elements of the input sequence, improve performance on sequential tasks, and handle long-range dependencies more effectively than traditional fixed-length representations.



### The Transformer "Attention is All You Need"

Paper published by a team at Google Brain.
- [Attention is All You Need](https://arxiv.org/abs/1706.03762)

The Transformer architecture is built on the idea of self-attention or scaled dot-product attention, which can be seen as an extension of the attention mechanism. In traditional sequence-to-sequence models, such as recurrent neural networks (RNNs), sequential information is processed step by step, which can be computationally expensive and hinder parallelization.

The key innovation of the Transformer is that it replaces recurrent layers with self-attention layers. Self-attention allows the model to compute the relationships between all positions in the input sequence simultaneously. This means that each position can attend to any other position, capturing global dependencies in the sequence. By doing so, the Transformer can process inputs in parallel and handle long-range dependencies more effectively.

The Transformer architecture consists of two main components: the encoder and the decoder. The encoder takes an input sequence and generates a sequence of contextualized representations, while the decoder takes the encoder's output and generates the final output sequence.

Within the encoder and decoder, the Transformer uses multi-head self-attention mechanisms. Instead of a single self-attention mechanism, multiple attention heads are employed to capture different types of information and attend to different parts of the input sequence simultaneously. This allows the model to focus on different aspects of the input and learn more diverse and expressive representations.

The Transformer also introduces positional encoding, which provides information about the position of each element in the input sequence. Since self-attention lacks the notion of position, positional encoding enables the model to incorporate sequential information into its computations.

The dominance of the Transformer architecture in modern AI can be attributed to several factors:

1. Parallelization: The self-attention mechanism in the Transformer enables parallel processing of inputs, making it highly efficient for training on modern hardware, such as graphics processing units (GPUs) or tensor processing units (TPUs).

2. Long-range dependencies: The self-attention mechanism allows the Transformer to capture dependencies between distant positions in the input sequence, making it more effective in modeling long-range relationships compared to traditional recurrent architectures.

3. Expressiveness: By employing multiple attention heads and capturing different types of information, the Transformer can learn more expressive and rich representations of the input data.

4. Transferability: The Transformer has shown strong performance across a wide range of NLP tasks, such as machine translation, language understanding, text generation, and more. Its effectiveness and versatility have made it a popular choice and a basis for many state-of-the-art models.

Overall, the Transformer's ability to model global dependencies, parallelize computations, and learn expressive representations has contributed to its dominance in modern AI, particularly in the field of natural language processing.


## Backpropogation

Backpropogation is an algorithm for training neural-networks, used to update its weights to minimize the 'loss'

1. Network makes a prediction on a batch of input data
2. Loss is calculated between predicted and actual output
3. Gradient of the loss with respect to the weights are calculated using the chain rule of differentiation
4. The gradients are used to update the weights in the opposite direction of the gradient, reducing the loss
5. Repeat the process until the loss reaches a satisfactory level or a maximum number of iterations

