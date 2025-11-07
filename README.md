## About me
I'm interested in AI, with a focus on Spiking Neural Networks (SNNs) and realtime learning. I don't think there's anything inherently special in human intelligence, and hence I think it can be computationally recreated. Since real-time learning occurs in biological systems through spiking mechanisms, I see SNNs as a promising direction toward achieving similar capabilities in artificial systems.

## Projects
### In Development:
- #### [traceTorch](https://github.com/Yegor-men/tracetorch)
A python library implementing eligibility propagation in an easy to use, PyTorch-esque manner.

- #### [ml-playground](https://github.com/Yegor-men/ml-playground)
My playground for various ML projects, in no specific order or grouping. I just got tired of having a billion repositories, needing to log each one while generally reusing a fair portion of the code, so from now on everything (unless it's something specific) will be in here instead.

- #### [S2IR](https://github.com/Yegor-men/S2IR)
Scale Invariant Image Refiner. Treats pixels like tokens, uses axial and cross attention with per-pixel conditioning and relative positional embedding, trained to predict noise like a diffusion model.

- #### [Pixelart Glyph Creator](https://github.com/Yegor-men/pixelart_glyph_creator)
A simple pixelart glyph creator for flexible sizes. Flexible rules with blacklisted and whitelisted kernels and symmetry rules. Creates an SQLite database of all valid glyphs, and then renders the glyphs from the database.

### Sunsetted:
Projects are classified into different categories:
 - 🧱 **Out of Scope**: projects that I stopped doing because (at the time of doing them) they were infeasible to me; lack of skill, hardware, anything that made me hit a wall.
 - 💥 **Failed Experiment**: projects that I started doing because I thought would work in theory, but did not in practice; it could maybe work with a rework, but I don't know.
 - 😴 **Abandoned**: projects that I abandoned out of loss of interest, regardless of their relative success or failure.
 - 🔁 **Superseded**: projects that work, they are technically funcitonal, but they are either impractical or the code is clumsy; if I haven't already I'd prefer to redo it from a clean slate.
 - ✅ **Completed**: projects that have fulfilled their duty; they work, there is nothing more to add to or gain from them.

- #### [BPOT (Back Propagation Over Time)](https://github.com/Yegor-men/BPOT-Back-Propagation-Over-Time) - 🔁 Superseded [Last commit on 30/07/2025]
A biologically plausible alternative to BPTT as long as neurons are able to send signals upstream, not just downstream. Given the technical simplicity of backpropagation (it's just value retrieval), in itself it's not that biologically implausible. All you do is just a forward and backward pass in one step, and hence you have backpropagation literally occuring over time, and everything is local.

Stopped because computationally, doing X amount of forward passes and the same X amount of backward passes takes the exact same amount of time regardless of if you're doing it in quick succession or a long chain. True parallelism doesn't exist, so in actuality doing one big forward pass and one big backward pass is actually faster than doing forward and backward for each layer. Also, the code gets clumsy, messy and doesn't particularly nicely tie in with default pytorch, now requiring a method to store the learning signal so that in the future backward pass it would use that instead. Just awkward with no practical payoff.

- #### [Scale Invariant Probabilistic Neurons](https://github.com/Yegor-men/Scale-Invariant-Probabilistic-Neurons) - ✅ Completed [Last commit on 17/06/2025]
A silly test on a scale invariant network literally driven by the synapse strength dictating the probability of the postsynaptic neuron firing. Based on [Artem Kirsanov](https://www.youtube.com/artemkirsanov)'s video on scale invariance.

Stopped because it's silly and obviously impractical. This was done just as a quick test. I hoped that it could somehow help me in figuring out some optimal synapse weight initialization for normal SNNs to also achieve the state of criticality and scale invariance, but it did not.

- #### [snntorch SLL](https://github.com/Yegor-men/snntorch-SLL) - 🔁 Superseded [Archived on 05/08/2025 but finished way earlier, around 01/06/2025]
I thought that I could get single lifetime learning (SLL) to work for flappy bird and pong by using snntorch.

Stopped when I realized that snntorch is not actually what I wanted. Enticed by the RTRL learning method that was advertized, snntorch in reality is no different from a manual implementation of an snn based recurrent model in base pytorch: it still builds out the massive computation graph and the rest, while what I wanted was true single lifetime learning without autograd graph building. I am, however, grateful for finding out about SNN networks because of snntorch.

- #### [Cyber Biological Neurons](https://github.com/Yegor-men/cyber_biological_neurons) - 🧱 Out of Scope [Last commit on 12/05/2025]
An incredibly naive idea of recreating one to one the base fundamentals of how biological neurons work, with the whole charge state being at -70mv etc.

Stopped because there's an insane amount of things to account for, and in actuality I had no idea how to make this learnable. Secondly, if I made it learnable, then what even is the point in trying to adhere to biology? I was also very naive, a classic example of the Dunning-Kruger effect.

- #### [replAI](https://github.com/Yegor-men/replAI) - 😴 Abandoned [Last commit on 30/04/2025]
A discord bot controlled by an LLM, intent being to give it maximal control over when and what messages to send, aiming to make it seem as realistic as possible.

Stopped because I realized that the amount of time it takes to fix prompt engineering and whatnot to accomodate for naturalness is simply not worth it; it's a certain level of uncanny valley because it's not good enough but too hard to make perfect, I've more interesting things to do and frankly a model trained specifically on this style would likely perform far better.

- #### [GPT2 recreation](https://github.com/Yegor-men/gpt2) - 🧱 Out of Scope [Last commit on 08/04/2025]
My attempt to recreate the GPT2 architecture, with the idea to do other transformer based models.

Stopped because I calculated that to train it fully I would require literal weeks of nonstop training on my local rig. I didn't want to idly sit so I stopped once I saw some progress in quality of output and it seemed like I got it right, the rest was just a matter of time.

- #### [Semantic de-duplication](https://github.com/Yegor-men/Semantic-De-duplication) - 🔁 Superseded [Last commit on 29/03/2025]
Finding text duplicates en masse by encoding each text, and then doing one matrix multiplication to see how similar each vector embedding is to each other one (literally the attention mechanism).

Stopped because I realized that AI implementations aren't really my thing, I like development more. Looking back it's probably garbage code as well, far too rashly written, no tests, nothing like that, would be better to rewrite anew rather than fix.

- #### [Transformer Stock Trader](https://github.com/Yegor-men/Transformer-Stock-Trader) - 🧱 Out of Scope [Last commit on 22/02/2025]
A transformer based model to look at stock history to try and predict the next pice to hence either buy or sell.

Stopped because I didn't actually properly know the transformer architecture, this was vibecoded. Also, obviously, if this worked, then every single company would be doing it, hence nullifying it's ability to work, hence it doesn't work.

- #### [Tic Tac Toe with reinfocement learning](https://github.com/Yegor-men/tic-tac-toe-rl) - 🔁 Superseded [Last commit on 11/02/2025]
A winged implementation or reinforcement learning with my intuitive understanding of it, not actually based on any real RL approach.

Stopped because the results were questionable. In that it works, sure, it does learn, but it would be better if it learned faster. Also, not an actual RL implementation, this was just a test on if I understand the principle correctly rather than actually making something to use later on.

- #### [Variable autoencoder](https://github.com/Yegor-men/vae) - 😴 Abandoned [Last commit on 10/02/2025]
Funnily enough, not an actual VAE, just an autoencoder. Idea was to recreate the SD 1.5 and SDXL VAE to then later make the actual diffusion models.

Stopped when I got more enticed by transformer models, and also annoyed by the rigidity of the size of acceptable resolutions.

- #### [Pytorch learning course made by Daniel Bourke](https://github.com/Yegor-men/learning-pytorch-from-daniel-bourke) - 😴 Abandoned [Last commit on 09/02/2023]
My repo for followin galong with Daniel Bourke's pytorch learning course. Stopped at the 13th hour or somewhere there.

- #### [Harmonic Loss paper](https://github.com/Yegor-men/harmonic-loss) - 💥 Failed Experiment [Last commit on 08/02/2023]
My implementation of the harmonic loss paper, the concept that for classification, the model is instead meant to predict an n sized vector, and then use the euclidean distance as the closeness to the nearest answer.

Stopeed because I kept getting NaNs and overflows, and I could not be bothered enough to fix them, especially considering that others reported the same thing too. Also conceptually it really shouldn't matter. The weights from the last layer to the classification neurons are already literally kind of doing that, what benefit does it give to give each output neuron it's own required vector?

- #### [Iris classification](https://github.com/Yegor-men/iris-classification) - ✅ Completed [Last commit on 08/02/2025]
The stape iris classification dataset.

- #### [MNIST](https://github.com/Yegor-men/mnist) - ✅ Completed [Last commit on 08/02/2025]
The stape MNIST problem.

- #### [Neural nets in raw python](https://github.com/Yegor-men/raw-python-neural-nets) - ✅ Completed [Archived on 09/02/2025 but finished way earlier, around 02/12/2023]
My first ever neural network, done entirely in raw python, and then with numpy. Done as a proof of concept of understanding backpropagation.

## Contact
It's best to contact me either via email or Twitter:
- email: yegor.mn@gmail.com
- [Twitter](https://x.com/Yegor_Men)

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
