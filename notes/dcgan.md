## Unsupervised Representation Learning with Deep Convolutional Generative Adversarial Networks

Combination of CNN and GAN. Shows that both generator and discriminator learns a hierarchy of representations from object parts to scenes and learned features can be applied as general image representations.

#### key points

* Replace any pooling layers with strided convolutions and fractional-strided convolutions
* Use only convolutional layers: called all convolutional net
* Validates result on three datasets: LSUN, Imagenet-1k and a newly assembled Faces dataset
* DCGAN + L2-SVM achieves significant results in classification tasks, although not state-of-the-art
* Walking through latent variables show that DCGAN didn't memorize images but learned representations from dataset
* By logistic regression on second highest convolutional layer, generator can forget to draw certain features
* By adding and subtracting z values of representations, generator adds and removes representations from results

#### thoughts

* Part that latent vector z can be arithmetically manipulated is amazing
    * It means z has successfully implied representations from images
* Integration with rnn might increase the clarity of the image generated (similar to DRAW)
* Fact that human's imaginated images in brain are not clear as well, to generate a clear image requires rnn for sure.
    * Generative model without rnn should be used in other areas like expectation of an object image
