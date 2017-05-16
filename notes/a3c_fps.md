## Training Agent for First-Person Shooter Game with Actor-Critic Curriculum Learning

Solving Doom AI problem with A3C & curriculum learning.

#### key points

* Uses batch-A3C
    * cumulate experiences from multi agents and update as batch
    * reduces bias
* One CNN extracts features from visual input for both policy and value function
    * adds game variables after extracted by CNN
    * splited to two FCs after adding game variables
* Encourages exploration
    * multiplying policy ouput of the network by an exploration factor before softmax
    * uniformly randomize the action for 10% random frames
* Curriculum learning
    * encourages agent to move and act in a certain way by introducing many small instant rewards
    * agent shifts toward easier or harder level depending on its performance - adaptive curriculum

#### thoughts

* Teaches an agent to move in a way architect wants
* too many parameters used..
* somewhere between supervised learning and reinforcement learning
* definitly not a general solution for fps games
