# librec-auto-demo2021

Configuration and data files for the librec-auto paper at CIKM'21

## Studies

This repository contains 5 studies that you can work with to understand the capabilities of ``librec-auto``. 

### demo01

This study illustrates basic usage of the system. For efficiency, we use a relatively small data set (FilmTrust) and curtail the learning process
to only 25 iterations. Two experiments are generated for item regularization weights of 0.001 and 0.01.

### demo02

The study is very similar to ``demo01`` but includes fairness-aware aspects of the system. We bring in a movie feature ("new") via the item features file and items with this feature are considered protected. We use the FAR reranker to promote these items in recommendation lists, and 