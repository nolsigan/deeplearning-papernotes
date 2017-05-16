## Learning from Demonstrations for Real World Reinforcement Learning

Real world RL problems, not like easily simulated other tasks, are hard to train from the bottom. This paper solves this issue by introducing DQfD (Deep Q-learning from Demonstrations). DQfD defines loss as combination of TD, supervised loss, and L2 regularization loss. DQfD starts training with pretraining step which only uses demonstration data. Then it starts cumulating its own experience in a different space and train by sampling from both demonstrated data and experienced data.

#### key points

* Method for integrating imitation learning and reinforcement learning
* Key is to use combined loss which not only enables imitation but also enables training after pretrain
* Pretraining accelerates early stage performance by a large margin
* After a long time, sometimes better performance than DDQN, rarely worse

#### thoughts

* It seems like making a good loss function is almost everything
* For many problems that take long time to train will have benefit from integrating this idea
    * Can it be integrated to learning-by-predicting??
