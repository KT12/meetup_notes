[Advanced`Spark and Tensorflow Meetup Group](https://www.meetup.com/Advanced-Spark-and-TensorFlow-Meetup-New-York/events/248201412/)

Chris Fregley - Pipeline AI, formerly of Netflix, Databricks

Google Cloud TPUs

All notebooks online community.pipline.ai

Started Pipline b/c not enough on prediction side of things
Chaos Monkey kills pods

TF is open source but you can see the higher version in Google Cloud before it drops. TF 1.8 has been available for about a month.  Optimized for TPUs.

(Similar to Databricks and Spark)

Need TPUEstimator to use same code on cluster and locally.

Checkout GoogleCloudPlatform Github for best practices / examples

If you use TPU, need to use TPUOptimizer so you can optimize across shards.

Each Github star is worth $1,500 in seed money, according to Silicon Valley VC.  About equal to sq foot cost of SF.

RedDwarf Github - maps followers.

Pipeline AI looks at both online and offline model optimization

Netflix very experimental.  Catching up with containers.  AMI based.

Don't productionaize something you can't measure.  Don't use Flask to serve.

Oscars were a big challenge for netflix.  Traffic and ML.

AWS spot instances dry up when CA goes to work at 10AM.

Volta V100 Tensorecore similar to TPUs.   If you want to activate Tensorcores to speed up forward prop, need to use matrices with dimension sizes of multiples of 8.

Tensorboard will now tell you how well your model will run on TPU's.