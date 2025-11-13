Collective cell migration is a hallmark of Dictyostelium discoideum behavior: when nutrients become scarce, thousands of otherwise independent amoeboid cells begin to self-organize, follow traveling cAMP waves, and ultimately converge into a multicellular aggregation center. These spatio-temporal patterns are richly expressed in microscopy movies, where early frames already contain subtle motion cues and wavefront signatures that foreshadow where the final aggregation “meeting spot” will form.

Specifically, this project aims to predict the future aggregation location(s) of Dicty using only the early portion of each movie. To accomplish this task, we need to address the following two challenging problems:

Handling the complexities of Dicty imaging data.
Dicty movies can vary widely in resolution, cell density, noise level, and even exhibit field-of-view drift. These factors introduce substantial variability across experiments, making raw frames difficult to compare or model directly. As a result, effective preprocessing—such as spatial registration and denoising is essential before any reliable sequence modeling can be performed.

Preserving spatial structure during sequence modeling (important).
Traditional sequence models (such as LSTMs and Transformers) are not inherently designed for images—their basic computational units operate on one-dimensional vectors. Consequently, a core challenge is designing a model that can capture long-range temporal dependencies without discarding fine-grained spatial information.

The code present a comprehensive evaluation of different spatiotemporal prediction models, examine their key components through ablation studies, evaluate their robustness, perform a variety of visualization analyses, and further introduce and refined a VAE-based framework to account for uncertainty in future-frame prediction.
