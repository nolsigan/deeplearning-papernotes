## Learning to Act by Predicting the Future

Instead of a monolithic state and a scalar reward, this paper consider a stream of sensory input and a stream of measurements. Assuming that the goal can be expressed in terms of future measurements, predicting these orivides all the information necessary to support action. This reduces sensorimotor control to supervised learning, while supporting learning from raw experience and without extraneous data.

#### key points

* Reinforcement Learning -> Supervised Learning
    * goal is expressed as measurements
    * predicting goal can be substituted by predicting measurements
    * predictor is trained by regression loss on predicting measurements
    * measurements are provided directly which enables supervised learning
* Model
    * three modules to encode natural inputs to a vector
        * image module, measurements module, goal module
    * encoded vector is then separated to expectation network and action network
        * expectation network for predicting expectation of the current state
        * action network for predicting advantages of each action
            * advantages are normalized to make expectation network predict average value of current state
* Goal vector is not definite
    * It doesn't have to be same for training and testing
    * It can be randomized during training time
    * randomizing helps predictor to generalize over different test goals

#### thoughts

* elegant idea
    * removes sparse reward problem that RL was suffering from
    * generalizes well
    * not many custom parameters needed
* wonder why training speed doesn't increase that much even though using supervised learning
    * maybe because training signal for action network only propagates on an action that's taken?
* there's no certain suggested way for choosing good goal vector
    * maybe predicting goal vector too may increase its performance or reduce training time