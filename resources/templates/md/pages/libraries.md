{:title "Libraries"
 :layout :page
 :page-index 4
 :navbar? true}

To supplement our opinionated blog posts analysing the ecosystem, here is a less-opinionated, plain list of relevant libraries written by Clojurians. Not all libraries mentioned here are affiliated with Scicloj, but we seek to be in dialogue with library authors as much as possible.

Do you know about anything relevant that is missing here? - [Let us talk](../about/#where)!

For every library, we mark whether it is actively developed (`act`), and whether it is still experimental (`exp`).

We tag libraries with the field they are relevant to.

* `array` - array programming
* `linalg` - linear algegra
* `native` - interop with native-optimized libraries
* `gpu` - gpu support
* `vis` - data visualization and visual art
* `lit` - literate programming
* `ui` - building UIs for data exploration
* `geo` - geographical and geometrical data processing
* `df` - dataframe-like data structures and abstructions
* `data` - general data processing
* `csv` - csv support
* `xform` - transducers support
* `math` - diverse math functions
* `stat` - statistics
* `ts` - time series analysis
* `rand` - simulation and random sampling
* `prob` - Bayesian computing and probabilistic programming
* `ml` - machine learning
* `dl` - deep learning
* `opt` - optimization
* `graph` - graph algorithms and network analysis
* `interop` - general libraries for interop
* `cljs` - supports not only Clojure but also Clojurescript

## Diverse toolsets
- [spork](https://github.com/joinr/spork) (`act`): `opt`,`df`,`vis`,`rand`,`graph`,`ui` - a toolbox for data-science and operation research
- [fastmath](https://github.com/generateme/fastmath) (`act`): `math`,`stat`,`rand`,`ml` - a collection of functions for mathematical and statistical computing, macine learning, etc., wrapping several JVM libraries
- [Incanter](https://github.com/incanter/incanter): `df`,`stat`,`vis`,`rand`,`csv` - an R-like data-science platform built on top of the core.matrix abstractions
- [huri](https://github.com/sbelak/huri): `df`,`stat`,`vis` - a toolbox for data-science using plain sequences of maps

## Array programming, linear algebra
- [tech.datatype](https://github.com/techascent/tech.datatype) (`act`): `array`,`native`,`stat` - abstractions and foundations for working with array-like structures and sequential structures
- [tvm-clj](https://github.com/techascent/tvm-clj) (`act`,`exp`): `array`,`linalg`,`native`,`gpu` - bindings to [tvm](https://github.com/apache/incubator-tvm)
- [Neanderthal](https://neanderthal.uncomplicate.org/) (`act`): `array`,`linalg`,`native`,`gpu` - matrix and linear algebra in Clojure
- [jutsu.matrix](https://github.com/hswick/jutsu.matrix): `array`,`linalg`,`native`,`gpu` - bindigs to [ND4J](https://deeplearning4j.org/docs/latest/nd4j-overview)
- [core.matrix](https://github.com/mikera/core.matrix): `array`,`linalg`,`native`,`cljs` - matrix abstractions, supporting diffent backends
- [denisovan](https://github.com/cailuno/denisovan): `array`,`linalg`,`native`,`gpu` - Neanderthal backend for core.matrix 

## Literate programming and data visualization
- [Hanami](https://github.com/jsa-aerial/hanami)(`act`): `vis`,`ui` - a template system for creating interactive data visualizations using Vega/Vega-lite, Reagent and Re-Com
- [Saite](https://github.com/jsa-aerial/saite) (`act`): `vis`,`lit`,`ui` - a literate programming application written using Hanami
- [Oz](https://github.com/metasoarous/oz) (`act`): `vis`,`lit` - data visuzliation using Vega/Vega-Lite and Hiccup, and a live-reload platform for literate-programming
- [Gorilla-REPL](http://gorilla-repl.org/): `lit` - a notebook application written in Clojure and Javascript
- [Gorilla-plot](https://github.com/JonyEpsilon/gorilla-plot): `vis` - plotting functions using Vega for Gorilla-REPL
- [Pink-Gorilla](https://github.com/pink-gorilla) (`act`,`exp`, temporary name): `vis`,`lit`,`ui`,`cljs` - a port of the Gorilla REPL project using a Clojurescript (Reagent) frontend
- [gg4clj](https://github.com/JonyEpsilon/gg4clj): `vis`,`r` - a clojure DSL for creating ggplot2 plots using R
- [Quil](https://github.com/quil/quil): `vis` - a clojure/clojuresctit wrapper for Processing 
- [cljplot](https://github.com/generateme/cljplot) (`act`,`exp`): `vis` - a data visualization platform written in Clojure and inspired by R's ggplot2 and lattice libraries
- [Devcards](https://github.com/bhauman/devcards): `lit`,`cljs`: visual repl exprience for Clojurescript
- [Maria](https://github.com/mhuebert/maria): `lit`, `vis`, `cljs`: a Clojurescript coding environment for beginners
- [Clojupyter](https://github.com/clojupyter/clojupyter) (`act`): `lit` - a Clojure kernel for Jupyter
- [IClojure](https://github.com/HCADatalab/IClojure): `lit` - a Clojure kernel for Jupyter
- [Notespace](https://github.com/scicloj/notespace) (`act`,`exp`): `lit` - notebook experience with Clojure namespaces edited at any editor

## Data processing
- [Specter](https://github.com/redplanetlabs/specter) (`act`): `data`,`cljs` - declarative navigation of nested data structures for selection and transformation in Clojure and Clojurescript
- [Meander](https://github.com/noprompt/meander) (`act`): `data`,`cljs` - transforming neseted data structures by declaratively declaring the shape of source and target datastructures
- [Odin](https://github.com/halgari/odin): `data` - processing nested data structures by extensible logic programming
- [xforms](https://github.com/cgrand/xforms): `data`,`cljs`,`xform` - a collection of transduces and reducing functions
- [Semantic Csv](https://github.com/metasoarous/semantic-csv): `csv`,`cljs` - higher level csv parsing/processing

## Geospatial processing 
- [geo](https://github.com/Factual/geo) (`act`): `geo` - unifying several JVM libraries for geoprocessing with a Clojure API
- [geo-clj](https://github.com/r0man/geo-clj) (`act`): `geo`,`cljs` - encoding/decoding of geographic datatypes 
- [aurelius](https://github.com/willcohen/aurelius) (`act`,`exp`): `geo`, `xform` - transducible analysis of geospatial features

## Dataframe-like structures
- [tech.ml.dataset](https://github.com/techascent/tech.ml.dataset) (`act`): `df`,`stat`,`vis`,`csv` - abstractions for dataframe-like structures in clojure, based on tech.datatype abstractions, with an implementation using the Tablesaw Java library
- [Panthera](https://github.com/alanmarazzi/panthera): `df`,`py` - a Clojure API wrapping Python's Pandas library
- [koala](https://github.com/aria42/koala) (`exp`): `df`,`csv` - Pandas-like data-processing for clojure with some I/O functionality
- [dataframe](https://github.com/ghl3/dataframe): `df` - Pandas-like data processing for clojure
- [danzig](https://github.com/ribelo/wombat) (formerly wombat) (`act`,`exp`): `df`,`xform` - Pandas-like data processing using transducers

## Statistics
- [kixi.stats](https://github.com/MastodonC/kixi.stats): `stat`,`rand`,`xform` - statistics and random sampling using transducers

## Time series analysis
- [tide](https://github.com/sbelak/tide) - `ts`: STL and FastDTW algorithms

## Bayesian computing, random sampling & probprog
- [inferme](https://github.com/generateme/inferme): `prob`,`rand`,`vis` - extensible probabilistic programming in Clojure itself (rather than a language variation), with support for visualizations
- [bayadera](https://github.com/uncomplicate/bayadera): `prob`,`gpu` - Bayesian computing using the GPU
- [sampling](https://github.com/bigmlcom/sampling): `rand` - support srandom sampling of different kinds
- [distributions](https://github.com/michaellindon/distributions): `rand`,`prob` - random sampling and some basic Bayesian computing for certain families of distributions
- [metaprob](https://github.com/probcomp/metaprob) (`exp`): `prob`,`rand`,`cljs` - an embedded languages for probabilistic programming and metaprogramming
- [anglican](http://probprog.ml/anglican/index.html): `prob`,`rand`,`cljs` - a probabilistic programming language written in clojure, that supports a subset of clojure

## Machine learning
- [tech.ml-base](https://github.com/techascent/tech.ml-base) (`act`): `ml` - a machine learning platform based on tech.ml.dataset, supporting not just ml algorithms, but also relevant ETL processing; wraps multiple machine learning libraries
- [clj-ml](https://github.com/joshuaeckroth/clj-ml/): `ml` - machine learning based on wrapping libraries such as the Weka Java library
- [clj-boost](https://gitlab.com/alanmarazzi/clj-boost): `ml` - a wrapper for XGBoost

## Deep Learning
- [MXNet](https://github.com/apache/incubator-mxnet/tree/master/contrib/clojure-package): `dl` - bindings to Apache MXNet - part of the MXNet project
- [Deep Diamond](https://github.com/uncomplicate/deep-diamond) (`act`): `dl`,`native`,`gpu` - infrastructure for tensor computation and deep learning
- [jutsu.ai](https://github.com/hswick/jutsu.ai): `dl` - a wrapper for deeplearning4j
- [Cortex](https://github.com/originrose/cortex): `dl` - a deep learning library written in Clojure
- [Flare](https://github.com/aria42/flare): `dl` - dynamic neural networks in Clojure

## Interop
- [Libpython-clj](https://github.com/clj-python/libpython-clj) (`act`): `interop` - interop with Python
- [Clojisr](https://github.com/scicloj/clojisr) (`act`): `interop` - interop with R and Renjin (R on the JVM)
- [graalvm-interop](https://github.com/davidpham87/graalvm-rinterop): `interop` - interop with FastR (GraalVM's R)
- [other R interop libraries](https://github.com/scicloj/clojisr/blob/master/doc/existing_libraries.md)
- [from-scala](https://github.com/t6/from-scala): `interop` - interop with Scala

## Big data & distributed processing
coming soon ..

