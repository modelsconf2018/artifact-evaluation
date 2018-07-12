# Expressive and Efficient Model Transformation with an Internal DSL of Xtend

The draft submitted for review at MODELS'18 can be found [here](https://yamtl.github.io/pubs/models18.pdf).

In the publication, we presented [Yet Another Model Transformation Language (YAMTL)](https://yamtl.github.io) and evaluated its performance with an adaptation of the VIATRA CPS benchmark framework. All of the software artifacts involved are available in [this public repository](https://github.com/yamtl/viatra-cps-batch-benchmark), including:
* pointers to the original benchmark;
* discussion on differences with the original benchmark;
* solutions used (their specification, their implementation, executable linked libraries, and instructions on how to use/modify them);
* raw results.

Note that raw results for the newly contributed solutions **may differ slightly** as we have updated the solutions with feedback obtained from the anonymous reviewers of MODELS'18. **These changes do not affect the conclusions stated in the paper.**

Additionally, two separate Gradle projects that illustrate how to use YAMTL for different model-to-model transformations are provided. These two projects include instructions on how to install (and run) them. The pointers to the projects are as follows: 
* [The transformation used in the benchmark](https://github.com/yamtl/examples/tree/master/yamtl.examples.mapping.batch.cps2dep): from cyberphysical systems to deployment models.
* [A mapping from simple class diagrams to simple relational schemas](https://github.com/yamtl/examples/tree/master/yamtl.examples.mapping.batch.cd2db).