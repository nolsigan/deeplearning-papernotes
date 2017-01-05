## Auto-Encoding Variational Bayes

Lack of Bayesian network knowledge to fully understand the paper. (Need to study!)

Shows that a reparameterization of the variational lower bound yields a lower bound estimator 
that can be straightforwardly optimized using standard stochastic gradient methods.
Shows that for i.i.d. datasets with continous latent variables per datapoint, posterior inference can be made
especially efficient by fitting an approximate inference model to the intractable posterior using the proposed lower bound estimator.

Good blog post about vae : [What is variational autoencoder](https://jaan.io/what-is-variational-autoencoder-vae)

#### key points (from blog post)

* Consists of two parts, encoder that compress the input data and decoder that generates output trying to minimize the loss in the whole process
* Loss function is the negative log-likelihood with a regularizer
* Because there are no global representations that are shared by all datapoints, we can decompose loss function and apply stochastic gradient descent
* Inferring good values of the latent variables(p(z|x)) requires exponential time to compute when trying exact inference
* Use Kullback-Leibler divergence to approximate the true posterior but it's also impossible to compute directly because of intractable variables
* Maximizing Evidence Lower BOund(ELBO) is equivalent to minimizing Kullback-Leibler divergence

#### thoughts

* Too much math! OTL.. Can't understand fully how loss function is generated
* Wonder how this method is applied in real life apps

