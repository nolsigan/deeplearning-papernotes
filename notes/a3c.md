## Asynchronous Methods for Deep Reinforcement Learning

It was previously thought that the combination of simple online RL algorithms with deep neural networks were fundamentally unstable. Recent works solved this issue by using experience replay but limited for off-policy algorithms. This paper introduces a simple idea that uses asynchronous gradient descent for optimization.

#### key points

* Recent success on deep reinforcement learning is limited to off-policy algorithms
    * on-policy methods are unable to use experience replay
    * without experience replay, high non-stationarity, strongly correlated
* Run multiple agents in parallel
    * globally shared parameters
    * each agent updates shared parameters every update cycle
* simple idea, reduces non-stationarity, decorrelates updates

#### thoughts

* Simple idea, large effect
* AI version of collective intelligence
