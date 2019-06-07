{:title "Are we scientists yet?"
 :layout :post
 :toc true
 :author "Alan Marazzi"
 :tags  ["data science"]}

The Clojure community is moving a lot lately on the data science front, but we were feeling we needed some organization and more open discussion about these themes. [This is the Clojureverse thread](https://clojureverse.org/t/online-meeting-clojure-data-science/3503) that started it all. Here we try to collect and record the current state of things, and I would like to stress the fact that this is owned by the community!

The structure of this:

- **Name of the problem** - data science is a stack of problems and one **must** have solutions to all of them to really be productive
- **Notable examples** - what's considered standard nowadays in other languages
- **Status** - the current status of the matter
- **Next** - the next best actions

# Multidimensional arrays, Linear-algebra

Generic computation libraries. Here we should strive for the best: both GPU and CPU capability, multidimensional arrays, broadcasting, etc

## Notable examples

- [Numpy](http://www.numpy.org/)
- [ND4J](https://deeplearning4j.org/docs/latest/nd4j-overview)

## Status

There are many libraries popping out at various levels of maturity, **some** of them are:

- [Neanderthal](https://neanderthal.uncomplicate.org/)
- [tvm-clj](https://github.com/techascent/tvm-clj)
- [tech.datatype](https://github.com/techascent/tech.datatype)
- [jutsu.matrix](https://github.com/hswick/jutsu.matrix)
- [core.matrix](https://github.com/mikera/core.matrix)
- [denisovan](https://github.com/cailuno/denisovan)

## Next

We probably don't need more libraries in this realm. What would be great next is:

- **Extended docs** - Something like https://docs.scipy.org/doc/numpy/index.html
- **Tutorials** - Common use cases, advanced stuff, etc
- **Bridges & extensions** - Libraries and packages connecting these frameworks to ther libraries or extending their functionality

# Plotting

Plotting is important for both analysis and presentation of results. Thanks to Clojurescript we might probably have an edge over other languages here.

## Notable examples

- [ggplot2](https://ggplot2.tidyverse.org/)
- [matplotlib](https://matplotlib.org/)
- [plotly](https://plot.ly/)

## Status

Here there are many libraries as well, **some** of them are:

- [Saite](https://github.com/jsa-aerial/saite)/[Hanami](https://github.com/jsa-aerial/hanami)
- [Oz](https://github.com/metasoarous/oz)
- [gorilla-plot](https://github.com/JonyEpsilon/gorilla-plot)
- [Quil](https://github.com/quil/quil)
- [cljplot](https://github.com/generateme/cljplot)

## Next

There's a lot of active development in this realm, what would be helpful:

- **Tutorials** - Common use cases, advanced stuff, etc

# Geospatial library

Deal with coordinates on a map.

## Notable examples

- [GeoPy](https://geopy.readthedocs.io/en/stable/)
- [mapnik](https://mapnik.org/)

## Status

There's something in this realm, mostly dated:

- [geo](https://github.com/Factual/geo)
- [clj-jts](https://github.com/jsofra/clj-jts)
- [cljts](https://github.com/sunng87/cljts)
- [mapnik-jni](https://clojars.org/forma/mapnik-jni)

## Next

This is another area where Clojure could shine thanks to its concurrency model. The fact it would be easy to deal with [Spark](https://spark.apache.org/) or [Onyx](https://github.com/onyx-platform/onyx) it's certainly a plus in case you have big data, while for smaller things parallel Clojure might be enough and speed up pipelines considerably.

- **Libraries** - This is an area where we are still lacking
- **Pluggability** - It would be very interesting to see libraries built on top of Spark or similar
- **New things** - Tooling in this space is very primitive even for more mainstream languages, people most of the time end up with bash scripts doing most of the work and gluing stuff together. This realm is a possible win for Clojure if we're able to come up with better solutions than other languages

# Dataframe or similar

Today's data scientists are used to work with tabular data, we have to deal with it.

## Notable examples

- [pandas](https://pandas.pydata.org/)
- [R](https://www.r-project.org/)
- [Arrow](https://arrow.apache.org/)

## Status

The picture has improved lately, but there still isn't consensus.

- [incanter](https://github.com/incanter/incanter)
- [huri](https://github.com/sbelak/huri)
- [koala](https://github.com/aria42/koala)
- [dataframe](https://github.com/ghl3/dataframe)
- [wombat](https://github.com/ribelo/wombat)
- [tech.ml-base](https://github.com/techascent/tech.ml-base)
- [spork](https://github.com/joinr/spork)

## Next

- **Extended docs** - Something like https://pandas.pydata.org/pandas-docs/stable/
- **Tutorials** - Common use cases, advanced stuff, etc
- **Bridges & extensions** - Libraries and packages connecting these frameworks to ther libraries or extending their functionality

# Graphs

Graphs can smartly and efficiently solve many problems, most of the time a well thought and built graph can substitute much more complex solutions

## Notable examples

- [GraphEngine](https://github.com/Microsoft/GraphEngine)
- [neo4j](https://neo4j.com/)
- [grph](http://www.i3s.unice.fr/~hogie/software/index.php?name=grph)
- [orientdb](https://github.com/orientechnologies/orientdb)

## Status

The state of things is pretty good and it makes sense considering the native Clojure data structures and the nature of graphs

- [neo4j-clj](https://github.com/gorillalabs/neo4j-clj)
- [clj-odbp](https://github.com/7bridges-eu/clj-odbp)
- [loom](https://github.com/aysylu/loom)
- [ubergraph](https://github.com/Engelberg/ubergraph)
- [corallo](https://github.com/7bridges-eu/corallo)

## Next

Graphs are mostly a solved problem, but only lately they are starting to be used extensively and there are many improvements that can be achieved in distributing graphs

- **Extend** - Considering that [GraphEngine](https://github.com/Microsoft/GraphEngine) runs on the CLR it should be possible (and very interesting) to get a Clojure API
- **Tutorials** - Let's show people the power of weilding graphs and Clojure together!

# Statistics & probprog

Very important as the base for ML systems MCMC simulations and data analytics.

## Notable examples

- [scipy](https://www.scipy.org/)
- [scikit-learn](https://scikit-learn.org/)
- [R](https://www.r-project.org/)
- [TensorFlow probability](https://github.com/tensorflow/probability)

## Status

There are already many examples:

- [kixi.stats](https://github.com/MastodonC/kixi.stats)
- [fastmath](https://github.com/generateme/fastmath)
- [huri](https://github.com/sbelak/huri)
- [bayadera](https://github.com/uncomplicate/bayadera)
- [sampling](https://github.com/bigmlcom/sampling)
- [anglican](http://probprog.ml/anglican/index.html)
- [distributions](https://github.com/michaellindon/distributions)
- [metaprob](https://github.com/probcomp/metaprob)

## Next

The main building blocks are all here, what we are missing are:

- **Bridges** - At least some of these libraries should be able to seamlessly communicate among them and with [dataset abstractions](#dataframe-or-similar) and with [arrays](#multidimensional-arrays,linear-algebra). Ideally we would have one of these able to run on GPU either directly (like bayadera) or through [MxNet](#deep-learning)
- **Extensions** - Better and easier abstractions. For instance a function to easily calculate ROC-AUC
- **Extended docs** - Something like https://pandas.pydata.org/pandas-docs/stable/
- **Tutorials** - Common use cases, advanced stuff, etc
- **Gradients** - There's still nothing around based on gradient descent, it would be really cool to get something like [TensorFlow probability](https://github.com/tensorflow/probability) in the [MxNet](https://mxnet.apache.org/api/clojure/index.html) realm

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
- [tech.ml](https://github.com/techascent/tech.ml)
- [tech.xgboost](https://github.com/techascent/tech.xgboost)
- [consimilo](https://github.com/andrewmcloud/consimilo)

## Next

We can still decide wether we want to pursue an [R](https://www.r-project.org/) model (with many small libraries) or the [scikit-learn](https://scikit-learn.org/) way (one big framework with batteries included), the important thing should be to have a common interface to algorithms and utilities. 

This would be the opposite of what happens in the R world, where developers and researchers are more free to deliver their ideas (R is usually the first language to get implementations of new algorithms), but at the same time the cognitive overhead for users is pretty high.

- **Bridges** - At least some of these libraries should be able to seamlessly communicate among them and with [dataset abstractions](#dataframe-or-similar) and with [arrays](#multidimensional-arrays-linear-algebra)
- **Extensions** - More models, faster or more memory efficient training and so on
- **Extended docs** - Something like https://scikit-learn.org/stable/index.html
- **Tutorials** - Common use cases, advanced stuff, etc

# NLP

Natural Language Processing is at the bleeding edge at the moment, but Clojure is lagging behind at the moment.

## Notable examples

- [gensim](https://radimrehurek.com/gensim/)
- [spacy](https://spacy.io/)
- [nltk](https://www.nltk.org/)

## Status

There are mainly 2 libraries dealing with these things at the moment, and one is currently looking for maintainers:

- [clojure-opennlp](https://github.com/dakrone/clojure-opennlp)
- [clojurenlp](https://github.com/clojurenlp/core)

## Next

It might very well be that all we need is a couple of very thorough and dedicated libraries, but we're not there yet

- **Maintain** - `clojurenlp` is currently looking for maintainers, get in touch with them if you're interested
- **Extend** - increase the functionality and the performance

# Image processing

Before doing anything with CNNs you have to read, process and transform images. The state of things here is much better than for many of the other sections!

## Notable examples

- [scikit-image](https://scikit-image.org/)
- [opencv](https://opencv.org/)

## Status

We're basically ready to do anything we want with images!

- [MxNet](https://github.com/apache/incubator-mxnet/tree/master/contrib/clojure-package)
- [tech.opencv](https://github.com/techascent/tech.opencv)
- [eye-boof](https://github.com/boechat107/eye-boof)
- [imagez](https://github.com/mikera/imagez)

# Deep learning

Important for computer vision, NLP and other problems.

## Notable examples

- [TensorFlow](https://www.tensorflow.org/)
- [PyTorch](https://pytorch.org/)
- [MxNet](https://mxnet.apache.org/)

## Status

We're pretty much covered especially thanks to Carin Meier's work, what can be really improved are docs, examples and tutorials.

- [MxNet](https://mxnet.apache.org/api/clojure/index.html)
- [Cortex](https://github.com/originrose/cortex)
- [jutsu.ai](https://github.com/hswick/jutsu.ai)
- [Flare](https://github.com/aria42/flare)

## Next

- **Gluon** - Having access to the [Gluon API](https://github.com/gluon-api/gluon-api) in MxNet would be very useful


> **Disclaimer**
> None of the lists are to be considered complete, they are just *some* examples. Everything is amendable by the community, if you think something is missing, wrong, misplaced or anything else just let the community know!
