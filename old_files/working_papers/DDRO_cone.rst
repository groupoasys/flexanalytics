.. _DDRO_cone:

Data-Driven Distributionally Robust Optimization via Optimal Transport with Order Cone Constraints
=====================================================================================================
.. sectionauthor:: Adrian Esteban-Perez <AdrianEsteban@uma.es>

This is a summary of the work that can be found in `[1]`_.

Abstract
--------

We tackle stochastic programs affected by ambiguity about the
probability law that governs their uncertain parameters. Using Optimal Transport Theory, we construct an ambiguity set that exploits the knowledge about the distribution of the uncertain parameters that is provided by: i) sample data and ii) `a-priori` information on the order among the probabilities that the true data-generating distribution assigns to some regions of its support set.  Such an order is enforced by means of order cone constraints and can encode a wide range of information on the shape of the probability distribution of the uncertain parameters such as that related to monotonicity or multi-modality. We seek decisions that  are distributionally robust. In a number of practical cases, the resulting distributionally robust optimization (DRO) problem can be  reformulated as a finite convex problem  where the `a-priori` information  translates into linear constraints. Furthermore, our method inherits the finite-sample performance guarantees of the Wasserstein-metric-based DRO approach proposed in Mohajerin Esfahani and Kuhn (2018), while generalizing this and other popular DRO approaches. Finally, numerical experiments are designed to provide insight into the performance of our approach for the Newsvendor problem.

Main results
------------

Under construction


.. _[1]: https://arxiv.org/pdf/1903.01769.pdf







