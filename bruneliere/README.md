# Towards Scalable Views on Heterogeneous Model Resources

Our contribution is the ability to create views combining very large models from
heterogeneous resources (e.g., in-memory or from NeoEMF- or CDO-managed
databases).  These views can be navigated and queried like regular models.

A version of the accepted paper (with minor corrections after reviews) can be
found [here][paper] (please do not disseminate; we will upload the camera-ready
on HAL as soon as it is ready).

[EMF Views][] and [NeoEMF][] are compatible with both Eclipse and Maven builds,
and are licensed under EPL-2.0.  You can find installation instructions on their
respective websites.  EMF Views has an [online manual][emfviews-manual], and
NeoEMF has [a tutorial][neoemf-tuto] to get started.

The evaluation section of the paper focuses on benchmarks, where we show that we
can take advantage of backend-specific optimizations to mitigate the latency of
navigating resources on disk.  All the code used for running these benchmarks is
[here][bench].  You can reproduce the results using our [Docker image][] (see
[instructions][]).

A snapshot of all the tools is available on [ReMoDD][].

[paper]: http://fmdkdd.free.fr/scalable-views.pdf
[EMF Views]: http://www.atlanmod.org/emfviews/
[NeoEMF]: http://www.neoemf.com/
[neoemf-tuto]: https://github.com/atlanmod/NeoEMF/wiki/Get-Started
[emfviews-manual]: http://www.atlanmod.org/emfviews/manual/user.html
[bench]: https://github.com/atlanmod/scalable-views-heterogeneous-models
[Docker image]: https://hub.docker.com/r/atlanmod/scalable-views/
[instructions]: https://github.com/atlanmod/scalable-views-heterogeneous-models#running-the-benchmarks-with-the-docker-image
[ReMoDD]: http://remodd.org/content/towards-scalable-views-heterogeneous-model-resources
