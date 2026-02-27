## About me
I'm interested in AI, with a focus on Spiking Neural Networks (SNNs) and realtime learning. I don't think there's anything inherently special in human intelligence, and hence I think it can be computationally recreated. Since online learning occurs in biological systems through spiking mechanisms, I see SNNs as a promising direction toward achieving similar capabilities in artificial systems.

### Prized works:
- [traceTorch](https://github.com/Yegor-men/tracetorch): A strict, ergonomic, and powerful Spiking Neural Network (SNN) library for PyTorch.
- [Resolution Invariant Image Diffuser (R2ID)](https://github.com/Yegor-men/resolution-invariant-image-diffuser): A resolution invariant image resampler (R2IR) and a resolution invariant image diffusion model (R2ID), working on cloud point attention and relative coordinate positional embedding. 
- [Pixelart Glyph Creator](https://github.com/Yegor-men/pixelart-glyph-creator): A procedural binary pixelart glyph creator with flexible rules for templates, blacklist and whitelist kernels.

## Projects
Projects are split into three types:
- **ACTIVE:** Projects that I'm actively working on
- **INACTIVE:** Projects with potential that I may come back to or may drop
- **ARCHIVED:** Repositories that are archived for one reason or another, that I will not come back to no matter what.

### ACTIVE
These projects are in "active" development, meaning that whilst commits are not necessarily active, the projects themselves are on my mind.

- #### [traceTorch](https://github.com/Yegor-men/tracetorch)
A strict, ergonomic, and powerful Spiking Neural Network (SNN) library for PyTorch.

- #### [Resolution Invariant Image Diffuser (R2ID)](https://github.com/Yegor-men/resolution-invariant-image-diffuser)
A resolution invariant image resampler (R2IR) and a resolution invariant image diffusion model (R2ID), working on cloud point attention and relative coordinate positional embedding.

### INACTIVE
These are projects that used to be active, but I've put a pause on them, at least for now. They'll either go back to [ACTIVE](#active), or move to [ARCHIVED](#archived), depending on the vibe and further developments of other projects. Commits here are either absent or very sparse.

- #### [Resolution Invariant Gaussian Splatting Image Generator (RIGSIG)](https://github.com/Yegor-men/RIGSIG)
An evolution to RIID (R2ID), RIGSIG generates images by creating gaussian splats and subsequently sampling points to get the image.

- #### [Pixelart Glyph Creator](https://github.com/Yegor-men/pixelart-glyph-creator)
A procedural pixelart glyph creator with flexible rules for templates, blacklist and whitelist kernels.

- #### [ReplAI](https://github.com/Yegor-men/replAI)
An LLM connected to a discord bot to improve the immersiveness of classic chatbots.

- #### [ML playground](https://github.com/Yegor-men/ml-playground)
A simple playground for various ML projects, used for quick tests or experiments. I just got tired of having a billion repositories, so now they're all dumped into here. The occasional good idea gets its own repository to which I move the code.

### ARCHIVED
The repositories in this list are permanently archived. I will not come back to them, and even if I revisit the problem / idea they were trying to solve, I will instead make a new repository for it rather than working with old code.

There are various reasons as to why a project got archived:
 - 🧱 **Out of Scope**: projects that I stopped doing because (at the time of doing them) they were infeasible to me; lack of skill, hardware, anything that made me hit a wall.
 - 💥 **Failed Experiment**: projects that I started doing because I thought would work in theory, but did not in practice; it could maybe work with a rework, but I don't know.
 - 😴 **Abandoned**: projects that I abandoned out of loss of interest, regardless of their relative success or failure.
 - 🔁 **Superseded**: projects that work, they are technically funcitonal, but they are either impractical or the code is clumsy; if I haven't already I'd prefer to redo it from a clean slate.
 - ✅ **Completed**: projects that have fulfilled their duty; they work, there is nothing more to add to or gain from them.

Each project also features the **Last Meaningful Update** (LMU). It's an arbitrary date when I feel that I stopped implementing any actual ideas, commits beyond that date are what I consider to be aesthetic changes, not something actually novel.

The `README.md` of each of these projects is also edited to explain the context, workings, and the lessons learnt throughout the development; all in more detail (depends on the mood) than briefly stated here.

- #### [Backpropagation Over Time](https://github.com/Yegor-men/backpropagation-over-time) - 🔁 Superseded - LMU on [2025-07-30]
Layer by layer backpropagation with learning signals that occurs over time; biologically plausible.

- #### [Scale Invariant Probabilistic Neurons](https://github.com/Yegor-men/scale-invariant-probabilistic-neurons) - ✅ Completed - LMU on [2025-06-17]
Weights dictate the probability that a downstream neuron fires based on the condition that an upstream neuron fired.

- #### [snnTorch SLL](https://github.com/Yegor-men/snntorch-sll) - 🔁 Superseded - LMU on [2025-06-01]
Single Lifetime Learning (SLL) with SNN models with snnTorch.

- #### [Cyberbiological Neurons](https://github.com/Yegor-men/cyberbiological-neurons) - 🧱 Out of Scope - LMU on [2025-05-12]
Biological neurons recreated into code.

- #### [GPT2](https://github.com/Yegor-men/gpt2) - 🧱 Out of Scope - LMU on [2025-04-08]
GPT2 recreation.

- #### [Semantic De-duplication](https://github.com/Yegor-men/semantic-de-duplication) - 🔁 Superseded - LMU on [2025-03-29]
Find semantic duplicates in large databases.

- #### [Transformer Stock Trader](https://github.com/Yegor-men/transformer-stock-trader) - 🧱 Out of Scope - LMU on [2025-02-22]
Decoder-only transformer to predict stock prices.

- #### [RL Tic Tac Toe](https://github.com/Yegor-men/rl-tic-tac-toe) - 🔁 Superseded - LMU on [2025-02-11]
Intuitive RL on Tic Tac Toe.

- #### [Image Autoencoder](https://github.com/Yegor-men/image-autoencoder) - 😴 Abandoned - LMU on [2025-02-10]
CNN autoencoder.

- #### [Daniel Bourke PyTorch Course](https://github.com/Yegor-men/daniel-bourke-pytorch-course) - 😴 Abandoned - LMU on [2025-02-09]
Following along Daniel Bourke's PyTorch course.

- #### [Harmonic Loss](https://github.com/Yegor-men/harmonic-loss) - 💥 Failed Experiment - LMU on [2025-02-08]
My implementation of the Harmonic Loss paper.

- #### [Iris](https://github.com/Yegor-men/iris) - ✅ Completed - LMU on [2025-02-08]
The staple Iris dataset.

- #### [MNIST](https://github.com/Yegor-men/mnist) - ✅ Completed - LMU on [2025-02-08]
The staple MNIST dataset.

- #### [Raw Python Neural Networks](https://github.com/Yegor-men/raw-python-neural-networks) - ✅ Completed - LMU on [2023-12-02]
Neural networks in raw python lists and layer-by-layer backpropagation; later added numpy for speed.


## Contact
It is best to contact me via email: yegor.mn@gmail.com or [LinkedIn](https://www.linkedin.com/in/yegor-men/)

<!--
**Yegor-men/Yegor-men** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
