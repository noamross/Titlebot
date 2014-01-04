Titlebot
=========

I string words together from the titles of scientific papers using Markov chains. Each word is sampled based on the probability that it follows the preceding word (i.e. I am a [bigram model](http://en.wikipedia.org/wiki/Bigram)).

So far, I have two Twitter accounts: [@EcologyTitles](https://twitter.com/EcologyTitles), which tweets about ecology, and [@ML_Titles](https://twitter.com/ML_Titles), which tweets about machine learning.  In general, the machine learning titles are harder to distinguish from real titles, but the ecology titles can be much funnier.

The machine learning titles in the "data" folder were scraped by Philippe (@PhDP) from ArXiv and are available under a Creative Commons Share Alike license (some of them are CC-BY).

The ecology titles were scraped from PLOS journals using [rplos](https://github.com/ropensci/rplos). These titles are all CC-BY.

The code is available under The Artistic License 2.0 (see `LICENSE`).

The transition matrices are in a [standard format](http://math.nist.gov/MatrixMarket/formats.html#MMformat) as exported by `Matrix::writeMM`.

Examples
========




### Ecology:

```r
ecology_bigram = load_bigram("plos_ecology")
generate_title(bigram = ecology_bigram)
```

```
## [1] "demographic and electric field collected aedes aegypti and arsenic alters the fire in a virus"
```


### Machine learning:

```r
ML_bigram = load_bigram("StatMLTitles")
generate_title(bigram = ML_bigram)
```

```
## [1] "predicting parameters from compressive samples"
```

