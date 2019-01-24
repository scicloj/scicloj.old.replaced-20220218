{:title "Are we scientists yet?"
 :layout :post
 :toc true
 :tags  ["data science"]}

The Clojure community is moving a lot lately on the data science front, but we were feeling we needed some organization and more open discussion about these themes. [This is the Clojureverse thread](https://clojureverse.org/t/online-meeting-clojure-data-science/3503/65) that started it all. Here we try to collect and record the current state of things, and I would like to stress the fact that this is owned by the community!

I really like how the Nim community is [dealing with the same sorts of problems](https://github.com/nim-lang/needed-libraries/issues/77) we're facing, so I'll try the same thing here to foster discussion. We might want to move these things in their own topic in the future or on other platforms, but that's not the point right now.

The structure of this:

- **Name of the problem** - data science is a stack of problems and one **must** have solutions to all of them to really be productive
- **Notable examples** - what's considered standard nowadays in other languages
- **Status** - the current status of the matter
- **Forward** - what is needed moving forward

# Multidimensional arrays, Linear-algebra

Generic computation libraries. Here we should strive for the best: both GPU and CPU capability, multidimensional arrays, broadcasting, etc

## Notable examples

- [Numpy](http://www.numpy.org/)
- [ND4J](https://deeplearning4j.org/docs/latest/nd4j-overview)

## Status

There are many libraries popping out at various levels of maturity, **some** of them are:

- [Neanderthal](https://neanderthal.uncomplicate.org/)
- [tvm-clj](https://github.com/techascent/tvm-clj)
- [jutsu.matrix](https://github.com/hswick/jutsu.matrix)
- [core.matrix](https://github.com/mikera/core.matrix)
- [denisovan](https://github.com/cailuno/denisovan)

## Forward

I think we can all agree that this degree of spread is not good, all these libraries represent wasted time and resources that might be spent on moving further other parts of the stack. We should settle on one-two of them and move on.

# Plotting

Plotting is important for both analysis and presentation of results. Thanks to Clojurescript we might probably have an edge over other languages here.

## Notable examples

- [ggplot2](https://ggplot2.tidyverse.org/)
- [matplotlib](https://matplotlib.org/)
- [plotly](https://plot.ly/)

## Status

Here there are many libraries as well, **some* of them are:

- [Saite](https://github.com/jsa-aerial/saite)/[Hanami](https://github.com/jsa-aerial/hanami)
- [Oz](https://github.com/metasoarous/oz)
- [gorilla-plot](https://github.com/JonyEpsilon/gorilla-plot)
- [Quil](https://github.com/quil/quil)

## Forward

In this area taste is really important so it's more normal to have more spread over different libraries. What we should do is to work on what is already available and make the plotting experience seamless: 

```clojure
(bar my-data)
;=> nil
```
The result would be a bar chart with reasonable defaults.

# Geospatial library

Deal with coordinates on a map.

## Notable examples

- [GeoPy](https://geopy.readthedocs.io/en/stable/)
- [mapnik](https://mapnik.org/)

## Status

Not much that I'm aware of:

- [geo](https://github.com/Factual/geo)

## Forward

This is another area where Clojure could shine thanks to its concurrency model. The fact it would be easy to deal with [Spark](https://spark.apache.org/) or [Onyx](https://github.com/onyx-platform/onyx) it's certainly a plus.

# Dataframe or similar

Today's data scientists are used to work with tabular data, we have to deal with it.

## Notable examples

- [pandas](https://pandas.pydata.org/)
- [R](https://www.r-project.org/)
- [Arrow](https://arrow.apache.org/)

## Status

Not good: there are lots of stumps here and there but nothing has ever caught on. Some examples:

- [huri](https://github.com/sbelak/huri)
- [koala](https://github.com/aria42/koala)
- [tech.ml-base](https://github.com/techascent/tech.ml-base)

## Forward

Here I would move on wrapping [Arrow](https://arrow.apache.org/) which have to potential to become the standard in the recent future, but anything that works is very welcome!

# Statistics & probprog

Very important as the base for ML systems and evaluation of models.

## Notable examples

- [scipy](https://www.scipy.org/)
- [scikit-learn](https://scikit-learn.org/)
- [R](https://www.r-project.org/)

## Status

There are already many examples:

- [kixi.stats](https://github.com/MastodonC/kixi.stats)
- [fastmath](https://github.com/generateme/fastmath)
- [huri](https://github.com/sbelak/huri)
- [bayadera](https://github.com/uncomplicate/bayadera)
- [sampling](https://github.com/bigmlcom/sampling)
- [anglican](http://probprog.ml/anglican/index.html)

## Forward

What is missing here is the tooling: we need more abstractions over basic functionality. For instance a function to get the ROC-AUC score for model validation.

Also better docs and examples of what is achievable with these libraries.

# Machine learning

General modeling, the aim should be to have something simple, usable, reliable and with a consistent interface.

## Notable examples

- [scikit-learn](https://scikit-learn.org/)
- [XGBoost](https://github.com/dmlc/xgboost)

## Status

Something is moving lately in this area:

- [fastmath](https://github.com/generateme/fastmath)
- [clj-ml](https://github.com/joshuaeckroth/clj-ml/)
- [clj-boost](https://gitlab.com/alanmarazzi/clj-boost)
- [tech.ml-base](https://github.com/techascent/tech.ml-base)
- [tech.xgboost](https://github.com/techascent/tech.xgboost)

## Forward

As stated earlier either we pursue an [R](https://www.r-project.org/) model (with many small libraries) or the [scikit-learn](https://scikit-learn.org/) way (one big framework with batteries included), the important thing should be to have a common interface to algorithms and utilities. This would be the opposite of what happens in the R world.

# Deep learning

Important for computer vision, NLP and other problems.

## Notable examples

- [TensorFlow](https://www.tensorflow.org/)
- [PyTorch](https://pytorch.org/)
- [MXNet](https://mxnet.apache.org/)

## Status

We're pretty much covered especially thanks to Carin Meier's work, what can be really improved are docs, examples and tutorials.

- [MXNet](https://mxnet.apache.org/api/clojure/index.html)
- [Cortex](https://github.com/originrose/cortex)
- [jutsu.ai](https://github.com/hswick/jutsu.ai)
- [Flare](https://github.com/aria42/flare)

## Forward

Just build on what's already there


> # Disclaimer
> None of the lists are to be considered complete, they are just *some* examples. Of course these are my opinions, but everything is amendable by the community and I would really love to get a productive discussion about these topics. If you think something is missing, wrong, misplaced or anything else just let the community know!
> Yeah, I know about [Incanter](https://github.com/incanter/incanter), I didn't mention it on purpose, but if someone thinks that it is current and useful we can surely discuss it :smile:
