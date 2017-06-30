# Bayesian Deep Learning
## Thomas Wiecki
Director of Data Science, Quantopian
[Related Notes](http://twiecki.github.io/blog/2017/03/14/random-walk-deep-net/)
Galvanize
June 27, 2017

ML most used in feature extraction = hand crafted features.  Alphas
Then use classifier to set portfolio.  Could also use deep learning here.

Deep learning was (like image recognition) able to learn features without instruction.  RNN, LSTM, 1D CNN.

Quant finance has unique problems.  Non-stationary / concept drift.  Cat is a cat (object recognition), but markets change.  Signals change and become obsolete.
Usual solution is to retrain model on more recent data (retrain every t days).  However, old data could still be useful.  Deep learning needs a lot of data - unfortunate to throw away data.

2nd problem - uncertainty.  Models will allow predict something, instead of saying, unsure.  Unseen input causes erratic behavior.  Need uncertainty estimate of predictions.

Deep learning
* Great perf
* Learn alphas from data
- No point est
- Can't deal with uncertainty

Bayesian Modeling
* Principled uncertainty quantification
* Very flexible (can deal with non-stationarity)

Above two complement each other very well.

How parameters relate to data
Parameters >> Likelihood >> Data

Formula is simple but solving for prior is difficult (mathematically intractable)

Use PyMC3, probabilistic programming
Inference algos: MCMC (accurate but slow), ADVI (fast but less accurate)

Constraint on weights - up to you, really.  Informed by priors.  Use expert domain knowledge. Or use flat distro to be intellectually humble.

PyMC3 will give you distro and point (MLE).
Because you have a prior - posterior will be closer to the original weight than the MLE point estimate.  A form of regularization.
Uniform prior does not regularize.

Posteriors can have all kinds of crazy distros.  ADVI assumes normal.  MCMC can do non-normal.

If you care about prediction (vs model params), then the normality assumption is not a big deal.  [Why?]

Bernoulli likelihood needs (0,1) probability, so use sigmoid not tanh in output layer

Instead of minimizing error, maximizing prob of seeing the data
CV, Bayesian optimization are ways to grow network without overfitting

So far, didn't need probabilistic programming.  Get uncertainty surface for free by embedding neural network with Bayesian uncertainty.
Think of posterior as a histogram.

# Dealing with non-stationarity
Every quant finance guy thinks data is stationary
Instead of using same weights across time, allow weights to change over time
Random walk perceptron

Advantages
Can use all of your data
Everything works because it's Bayesian

1st layer rotates, deeper network layers learn the shape.