## Playing Atari with Deep Reinforcement Learning

Reinforcement learning + Deep learning! Proposes a way to integrate deep learning methods to RL and achieves state-of-the-art results in 7 Atari games.

#### key points

* Traditional RL methods relied on the quality of the feature representation
* Deep learning methods can extract high-level features from raw pixels but integrating with RL isn't intuitive
    * Successful deep learning methods required large labelled data but RL algorithms learn from sparse, noisy and delayed rewards
    * Data distribution changes as RL algorithms learn
* Because it's hard to directly apply deep learning to RL, this paper targets Q learning
    * Function Q gets sequence, action as input and returns future reward agent can get
    * Because calculating exact Q is impossible, finding approximate Q is a major problem
    * Approximate Q is represented as non-linear function and here is when Deep learning comes in
* One frame of raw pixels is not enough for judging the situation, so CNN receives N successive frames (called experience replay)
* Randomly selects minibatch of transitions from replay memory and updates CNN by stochastic gradient descent
* Same algorithm and parameters can be used in all 7 games and all of them achieves astonishing results

#### thoughts

* Deep learning can be applied to all kinds of area where regression analysis is needed but dimension is too high to compute
    * Finding method that solves problem by regression analysis is a key factor for using deep learning
    * Same for VAE methods (approximates variational inference)
    * Same for GAN (approximates raw pixels with lower dimensions)
* Somehow, RL needs to generalize its core parts like reward or policy
    * Think it's vital for RL to lead general AI