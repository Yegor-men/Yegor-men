## About me
I'm interested in AI, with a focus on Spiking Neural Networks (SNNs) and realtime learning. I don't think there's anything inherently special in human intelligence, and hence I think it can be computationally recreated. Since real-time learning occurs in biological systems through spiking mechanisms, I see SNNs as a promising direction toward achieving similar capabilities in artificial systems.

## Projects
### Currently working on:
- #### [tracetorch](https://github.com/Yegor-men/tracetorch)
The natural successor to [BPOT (Back Propagation Over Time)](https://github.com/Yegor-men/BPOT-Back-Propagation-Over-Time), tracetorch revolves around maintaining and using traces instead of autograd for backpropagation. The idea is that a trace is, by definition, a weighted running average, favoring temporally near events, and hence those that are most likely to affect the model. During the backward pass, as long as the traces and parameters could be used to estimate the "average" output of each layer, the recurrent model should in theory hence be able to compress an arbitrarily massive history into effectively one forward pass, without actually building the autograd graph. Also, the RL REINFORCE methodology now changes from "which actions lead to better rewards in the future" to "which actions in a greedy approach seem most profitable", which ideologically aligns closer to what we see in humans and their development: egotistical short term thinking that progressively expands into long term strategizing rather than the REINFORCE style long term strategizing from the get go.

- #### [ml-playground](https://github.com/Yegor-men/ml-playground)
My playground for various ML projects, largely revolving around textgen and imagegen, or anything else that appears along the way. Got tired of having a billion repositories for things that are already well known / implemented, so now they'll be in here instead.

### On hold / soon to start:


### Future projects:


### Sunsetted and why:
- #### [replAI](https://github.com/Yegor-men/replAI)
A discord bot controlled by an LLM, intent being to give it maximal control over when and what messages to send, aiming to make it seem as realistic as possible.

Stopped because I realized that the amount of time it takes to fix prompt engineering and whatnot to accomodate for naturalness is simply not worth it; it's a certain level of uncanny valley because it's not good enough but too hard to make perfect, I've more interesting things to do and frankly a model trained specifically on this style would likely perform far better.

- #### [BPOT (Back Propagation Over Time)](https://github.com/Yegor-men/BPOT-Back-Propagation-Over-Time)
A biologically plausible alternative to BPTT as long as neurons are able to send signals upstream, not just downstream. Given the technical simplicity of backpropagation (it's just value retrieval), in itself it's not that biologically implausible. All you do is just a forward and backward pass in one step, and hence you have backpropagation literally occuring over time, and everything is local.

Stopped because computationally, doing X amount of forward passes and the same X amount of backward passes takes the exact same amount of time regardless of if you're doing it in quick succession or a long chain. True parallelism doesn't exist, so in actuality doing one big forward pass and one big backward pass is actually faster than doing forward and backward for each layer. Also, the code gets clumsy, messy and doesn't particularly nicely tie in with default pytorch, now requiring a method to store the learning signal so that in the future backward pass it would use that instead. Just awkward with no practical payoff.

- #### [snntorch SLL](https://github.com/Yegor-men/snntorch-SLL)
I thought that I could get single lifetime learning (SLL) to work for flappy bird and pong by using snntorch.

Stopped when I realized that snntorch is not actually what I wanted. Enticed by the RTRL learning method that was advertized, snntorch in reality is no different from a manual implementation of an snn based recurrent model in base pytorch: it still builds out the massive computation graph and the rest, while what I wanted was true single lifetime learning without autograd graph building. I am, however, grateful for finding out about SNN networks because of snntorch.

- #### [Scale Invariant Probabilistic Neurons](https://github.com/Yegor-men/Scale-Invariant-Probabilistic-Neurons)
A silly test on a scale invariant network literally driven by the synapse strength dictating the probability of the postsynaptic neuron firing. Based on [Artem Kirsanov](https://www.youtube.com/artemkirsanov)'s video on scale invariance.

Stopped because it's silly and obviously impractical. This was done just as a quick test. I hoped that it could somehow help me in figuring out some optimal synapse weight initialization for normal SNNs to also achieve the state of criticality and scale invariance, but it did not.

- #### [Cyber Biological Neurons](https://github.com/Yegor-men/cyber_biological_neurons)
An incredibly naive idea of recreating one to one the base fundamentals of how biological neurons work, with the whole charge state being at -70mv etc.

Stopped because there's an insane amount of things to account for, and in actuality I had no idea how to make this learnable. Secondly, if I made it learnable, then what even is the point in trying to adhere to biology? I was also very naive, a classic example of the Dunning-Kruger effect.

- #### [GPT2 recreation](https://github.com/Yegor-men/gpt2)
My attempt to recreate the GPT2 architecture, with the idea to do other transformer based models.

Stopped because I calculated that to train it fully I would require literal weeks of nonstop training on my local rig. I didn't want to idly sit so I stopped once I saw some progress in quality of output and it seemed like I got it right, the rest was just a matter of time.

- #### [Semantic de-duplication](https://github.com/Yegor-men/Semantic-De-duplication)
Finding text duplicates en masse by encoding each text, and then doing one matrix multiplication to see how similar each vector embedding is to each other one (literally the attention mechanism).

Stopped because I realized that AI implementations aren't really my thing, I like development more. Looking back it's probably garbage code as well, far too rashly written, no tests, nothing like that, would be better to rewrite anew rather than fix.

- #### [Transformer Stock Trader](https://github.com/Yegor-men/Transformer-Stock-Trader)
A transformer based model to look at stock history to try and predict the next pice to hence either buy or sell.

Stopped because I didn't actually properly know the transformer architecture, this was vibecoded. Also, obviously, if this worked, then every single company would be doing it, hence nullifying it's ability to work, hence it doesn't work.

- #### [Tic Tac Toe with reinfocement learning](https://github.com/Yegor-men/tic-tac-toe-rl)
A winged implementation or reinforcement learning with my intuitive understanding of it, not actually based on any real RL approach.

Stopped because the results were questionable. In that it works, sure, it does learn, but it would be better if it learned faster. Also, not an actual RL implementation, this was just a test on if I understand the principle correctly rather than actually making something to use later on.

- #### [Variable autoencoder](https://github.com/Yegor-men/vae)
Funnily enough, not an actual VAE, just an autoencoder. Idea was to recreate the SD 1.5 and SDXL VAE to then later make the actual diffusion models.

Stopped when I got more enticed by transformer models, and also annoyed by the rigidity of the size of acceptable resolutions.

- #### [Iris classification](https://github.com/Yegor-men/iris-classification)
The stape iris classification dataset.

- #### [MNIST](https://github.com/Yegor-men/mnist)
The stape MNIST problem.

- #### [Harmonic Loss paper](https://github.com/Yegor-men/harmonic-loss)
My implementation of the harmonic loss paper, the concept that for classification, the model is instead meant to predict an n sized vector, and then use the euclidean distance as the closeness to the nearest answer.

Stopeed because I kept getting NaNs and overflows, and I could not be bothered enough to fix them, especially considering that others reported the same thing too. Also conceptually it really shouldn't matter. The weights from the last layer to the classification neurons are already literally kind of doing that, what benefit does it give to give each output neuron it's own required vector?

- #### [Pytorch learning course made by Daniel Bourke](https://github.com/Yegor-men/learning-pytorch-from-daniel-bourke)
My repo for followin galong with Daniel Bourke's pytorch learning course. Stopped at the 13th hour or somewhere there.

- #### [Neural nets in raw python](https://github.com/Yegor-men/raw-python-neural-nets)
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
