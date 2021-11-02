# librec-auto-demo2021

Configuration and data files for the librec-auto paper at CIKM'21

## Studies

This repository contains 5 studies that you can work with to understand the capabilities of ``librec-auto``. 

### demo01

This study, which was used in the CIKM conference presentation, illustrates basic usage of the system. For efficiency, we use a 
relatively small data set (FilmTrust) and curtail the learning process
to only 25 iterations. Two experiments are generated for item regularization weights of 0.001 and 0.01. This study also includes
fairness-aware re-ranking using the FAR re-ranker. The protected class of movies (for demonstration purposes) are "new" movies as
these turn out to be less often recommended in FilmTrust.

### demo02

The study is very similar to ``demo01`` but performs the optimization of both item and user regularization using Bayesian black box optimization
instead of search over fixed parameters. Re-ranking is not included. For demonstration purposes, only 10 iterations of optimization 
are performed, many more would be required to get a good sampling. Note that only floating point values can be optimized in this release.

### demo03

This study demonstrates the use of non-LibRec libraries for recommendation generation. We demonstrate the use of the variational autoencoder implementation in the Microsoft Recommenders library.

### demo04

This study demonstrate the use of non-LibRec evalulation metrics. We show an example using the Expected Exposure Loss metric from Diaz, et al. 2020. 

### demo05

This study demonstrates the handling of multiple feature types in `librec-auto`. We specify two protected features and use one for evaluation and a different one for re-ranking to see how the re-ranking on a provider-side criterion impacts consumer-side fairness.

##  Data

The data used in all of these examples is the FilmTrust data that is distributed with the LibRec library.
