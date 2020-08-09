{:title "Are we scientists yet?"
 :layout :post
 :toc true
 :author "???"
 :tags  ["data science"]}

# Intro

This post is a continuation of two blog posts written by Alan Marazzi in the first half of 2019: [2019-01-21](https://scicloj.github.io/posts/2019-01-21-clojure-scientists/), [2019-05-23](https://scicloj.github.io/posts/2019-05-23-clojure-scientists/). Alan's idea was to analyse the state of the Clojure data science ecosystem, as a starting point for discussion. Indeed his analysis did encourage [fruitful community discussion](https://clojureverse.org/t/online-meeting-clojure-data-science/3503/11?u=daslu) back then. Here we attempt having a fresh look at the current situation.

The nature of this post is a bit different. We mainly offer an opinionated list of projects worth following, and directions worth developing. Hopefully, it can serve as a decent intro for a newcomer willing to stat exploring. For a more comprehensive list of libraries, see our [Libraries page](../pages/libraries). 

If you are interested in joining this discussions and the efforts to build the ecosystem, you are invited to the [data science stream at the Clojurians Zulip](https://clojurians.zulipchat.com/#narrow/stream/151924-data-science).

# Multidimensional arrays, Linear-algebra

- [Neanderthal](https://neanderthal.uncomplicate.org/) is a library for linear algebra and array programming, based on optimized native libraries code for the CPU and the GPU.

- [tech.datatype](https://github.com/techascent/tech.datatype) is a set of abstractions for working with array-like structures. Among other things, it allows zero-copy integration with libraries such as Neanderthal, as well as with non-JVM libraries such as Numpy and Apache Arrow.

- [tvm-clj](https://github.com/techascent/tvm-clj) is a set of Clojure bindings for Apache TVM -- a compiler stack for deep learning systems.

## Optimization
https://github.com/atisharma/matlib
- optimisation and control theory tools and convenience functions based on Neanderthal.

## Time series
This is still one of the missing pieces in the emerging ecosystem.
We are mentioning it here since o e 


## Geospatial data 

JTS
- [geo](https://github.com/Factual/geo)
Planning to integrate with tech.ml.dataet .

# Big Data

JVM
This is another area where Clojure could shine thanks to its concurrency model. The fact it would be easy to deal with [Spark](https://spark.apache.org/) or [Onyx](https://github.com/onyx-platform/onyx) it's certainly a plus in case you have big data, while for smaller things parallel Clojure might be enough and speed up pipelines considerably.

Spark: Flambo, Sparkling, Geni

Kafka and Kafka Streams: Jackdaw, kafka.clj

# Dataframes

Today's data scientists are used to work with tabular data.

[tech.ml.dataset](https://github.com/techascent/tech.ml.dataset) offers an dataframe-like entities based on the tech.datatype abstractions mentioned above.

[tablecloth](https://github.com/scicloj/tablecloth) wraps tech.ml.dataset with a user-friendly API.

# Graphs
- [neo4j-clj](https://github.com/gorillalabs/neo4j-clj)
- [loom](https://github.com/aysylu/loom)
- [ubergraph](https://github.com/Engelberg/ubergraph)

# Statistics
- [kixi.stats](https://github.com/MastodonC/kixi.stats)
- [fastmath](https://github.com/generateme/fastmath)
-
# Probabilistic programming and Bayesian computing
- [bayadera](https://github.com/uncomplicate/bayadera)
- [inferme](https://github.com/generateme/inferme)

# Machine learning
- [Smile](https://github.com/haifengl/smile)
- [fastmath](https://github.com/generateme/fastmath)
- [tech.ml](https://github.com/techascent/tech.ml)

# Computer Vision
- [tech.opencv](https://github.com/techascent/tech.opencv)

# Deep learning
- [MxNet](https://mxnet.apache.org/api/clojure/index.html)
- [Deep Diamond](https://github.com/uncomplicate/deep-diamond)

# Data visualization

Thanks to Clojurescript, Clojure may have an edge over other other languages in fast developments of DSLs for data visualization.

- /[Hanami](https://github.com/jsa-aerial/hanami)
- [Oz](https://github.com/metasoarous/oz)
- [gorilla-plot](https://github.com/JonyEpsilon/gorilla-plot)
- [Quil](https://github.com/quil/quil)
- [cljplot](https://github.com/generateme/cljplot)
- [gorilla-ui]
- [tech.viz](https://github.com/techascent/tech.viz)
- [goldly]
- [Hanami](https://github.com/jsa-aerial/hanami)
- [Quil](https://github.com/quil/quil)
- [thi-ng/geom](https://github.com/thi-ng/geom)
- [Portal](https://github.com/djblue/portal)
- [Reveal](https://github.com/vlaaad/reveal)

# Notebooks and Literate programming
Here there are several active projects, in various stages of maturity.

- [Pink Gorilla](https://github.com/pink-gorilla) is a revival of the classic [Gorilla-REPL](http://gorilla-repl.org/) project, on a modern Clojurescript stack, with lots of extensions in the UI, the functionality and the setup around it.

- [Saite](https://github.com/jsa-aerial/saite)

- [Oz](https://github.com/metasoarous/oz)

- [Clojupyter](https://github.com/clojupyter/clojupyter)

- [Notespace](https://github.com/scicloj/notespace)

Atom Chlorine
rmarkdown-clojure

# Interop

[Libpython-clj](https://github.com/clj-python/libpython-clj) is probably the most advanced solution for calling Python in the JVM. It offers nice features such as zero copy, a DSL embracing the Python internals in a Clojury way, and powerful functionality for exploring python packages, modules, classes and objects. It has already attracted lots of attention in the Clojure ecosystem, and there have already been serious experiments in using it for Computer Vision, NLP and other uses.

[ClojisR](https://github.com/scicloj/clojisr) is the main solution for calling R in Clojure. It offers a DSL for writing R code as Clojure data structures, and a detailed data-conversion functionality embracing tech.ml.dataset. The current developments efforts are in making multi-session support more robust, by making computations reproducible and by caching intermediate results. This will allow a lightweight way to orchestrate multiple R sessions and share data across them.
