# Master's Dissertation: Investigating the Impact of Entropy Regularisation on an Attention Augmented Agent

## Overview
This repository contains the research conducted for my master's dissertation, which investigates the impact of entropy regularisation on reinforcement learning (RL) agents. The project aims to attempt to identify optimal entropy coefficients that maximise learning and stability in three different Atari environments: Space Invaders, Seaquest, and Breakout.

## Abstract
In reinforcement learning, the balance between exploration and exploitation is crucial for effective training. Entropy regularisation is a technique used to promote exploration and prevent the convergence to sub-optimal policies by introducing stochasticity in policy distributions. This research focuses on how varying entropy regularisation coefficients affect the learning outcomes and stability of an RL agent augmented with an attention module. Through experimentation with various entropy coefficients and decay strategies, it was found that decaying entropy typically offers better performance than static entropy settings. Additionally, the complexity added by the attention network was evaluated to determine its impact on the agent’s learning capabilities. The findings indicate a correlation between increased network complexity and the degradation of learning efficiency.

## Key Experiments
- **Entropy Coefficients**: Various coefficients were tested to determine which configurations yield the best results in terms of learning performance and stability.
- **Decay Strategies**: Both static and dynamic entropy configurations were explored, with particular focus on understanding their impact across different game environments.
- **Attention Mechanism**: The attention-augmented agent's decision-making processes were visualised using attention maps and provides insight into the influence of entropy regularisation on attention patterns.

## Results

The experiments conducted show that entropy regularisation is an important mechanism to improve an agent’s ability to explore. The results of the experiments indicate that the decaying entropy coefficients generally led to improved performance across all environments when compared to the static entropy coefficients. It was also observed that the overall stability of the agent was improved when tested over multiple runs, compared to the agents which were configured with static entropy coefficients. This research also investigated whether a single entropy coefficient could be applied across various environments to consistently improve performance. The findings suggest that, while the commonly used static entropy coefficient of 0.01 does result in decent performance, decaying entropy coefficients, specifically a decay from 0.05 – 0.01, often outperform the static coefficients. This data suggests that while a static entropy coefficient of 0.01 can be effective, more dynamic control of the entropy coefficient could be beneficial in producing more optimal agents.

The inclusion of the attention network within the RL model was shown to significantly increase the qualitative interpretability of the models’ decisions by providing a means of deciphering what the agent is attending to as it learns the environment. As one of the main criticisms of deep learning is their “black box” nature, through the use of attention maps to demystify the decisions being made by an agent, it enables both experts and non-experts to get a high-level insight into what the agent is learning. While by no means perfect, the use of attention maps may be considered a step in the right direction towards creating more interpretable and understandable models. This, in turn, can help build trust in deep learning, especially in areas where it can have significant consequences, i.e., healthcare. Unfortunately, with the increased interpretability also came degraded performance due to the increased complexity and depth of the network. This research showed that a trade-off emerged between interpretability and performance following the introduction of the attention mechanism. This trade-off is a problem for real world applications such as in healthcare, where interpretability is necessary but performance cannot be sacrificed just to have a more interpretable model. There are potential ways to resolve these performance issues, and the findings from the literature suggest that attention models can achieve competitive results compared with state- of-the-art models (Mott et al., 2019), although this was not observed in these experiments.

For future work, the number of environments tested could be increased to see if a generalisable entropy coefficient, such as the decay from 0.05 – 0.01, continues to show promising results. Complexity of the action space and environment complexity could also be increased to examine whether decaying entropies continue to outperform static entropies when the dimensional complexity increases. The performance degradation of the attention augmented RL model caused by increased depth and complexity of the network is also something to be explored, potentially by incorporating techniques such as identity mapping from the D2RL architecture (Sinha et al., 2020). Furthermore, increasing the number of repeated runs for an agent in a given environment would provide better aggregated performance information. Alternative architectures for the model could also be explored to see if there is a more optimal model configuration which facilitates increased performance.

### Breakout Comparative Average Reward with Varying Entropy Coefficents

The comparative average rewards with varying entropy coefficients in the Breakout environment:

![Breakout Comparative Average Reward](https://github.com/maguid28/MSc-AttentionAugmentedRL/blob/main/results/Breakout%20Comparative%20Average%20Reward.png "Breakout Comparative Average Reward")

![Breakout Comparative Best Run](https://github.com/maguid28/MSc-AttentionAugmentedRL/blob/main/results/Breakout%20Best%20Run%20Comparison.png "Breakout Comparative Best Run")

![SpaceInvaders Comparative Average Reward](https://github.com/maguid28/MSc-AttentionAugmentedRL/blob/main/results/Breakout%20Comparative%20Average%20Reward.png "SpaceInvaders Comparative Average Reward")

![SpaceInvaders Comparative Best Run](https://github.com/maguid28/MSc-AttentionAugmentedRL/blob/main/results/Breakout%20Best%20Run%20Comparison.png "SpaceInvaders Comparative Best Run")

![Seaquest Comparative Average Reward](https://github.com/maguid28/MSc-AttentionAugmentedRL/blob/main/results/Breakout%20Comparative%20Average%20Reward.png "Seaquest Comparative Average Reward")

![Seaquest Comparative Best Run](https://github.com/maguid28/MSc-AttentionAugmentedRL/blob/main/results/Breakout%20Best%20Run%20Comparison.png "Seaquest Comparative Best Run")


## Video Demonstration
A video demonstration of the visualized attention maps and the agent's performance across different settings and environments can be viewed [here](https://www.youtube.com/watch?v=hS4bjPz-kGw).


## Keywords
`Reinforcement Learning`, `Entropy Regularisation`, `Exploration-Exploitation Balance`, `Attention`, `Attention Maps`, `Hyperparameter Tuning`

## Citation
If you find this research useful or refer to it in your academic or professional work, please consider citing it.

Maguire, D. (2024). Master's Dissertation: Investigating the Impact of Entropy Regularisation on an Attention Augmented Agent. [Source code]. https://github.com/maguid28/MSc-AttentionAugmentedRL


