.. _PBDROOTOCC_TPWRS:

Partition-based Distributionally Robust Optimization via Optimal Transport with Order Cone Constraints
======================================================================================================
.. sectionauthor:: Lisa Huckfield <tradrev12@gmail.com>

This is a summary of the work that can be found in `[1]`_. Open Access pdf is available at `[2]`_.

Abstract
--------

In this paper we wish to tackle stochastic programs affected by ambiguity about the probability law that governs their uncertain parameters. Using optimal transport theory, we construct an ambiguity set that exploits the knowledge about the distribution of the uncertain parameters, which is provided by: (1) sample data and (2) a-priori information on the order among the probabilities that the true data-generating distribution assigns to some regions of its support set. This type of order is enforced by means of order cone constraints and can encode a wide range of information on the shape of the probability distribution of the uncertain parameters such as information related to monotonicity or multi-modality. We seek decisions that are distributionally robust. In a number of practical cases, the resulting distributionally robust optimization (DRO) problem can be reformulated as a finite convex problem where the a-priori information translates into linear constraints. In addition, our method inherits the finite-sample performance guarantees of the Wasserstein-metric-based DRO approach proposed by Mohajerin Esfahani and Kuhn (Math Program 171(1–2):115–166. https://doi.org/10.1007/s10107-017-1172-1, 2018), while generalizing this and other popular DRO approaches. Finally, we have designed numerical experiments to analyze the performance of our approach with the newsvendor problem and the problem of a strategic firm competing à la Cournot in a market.


Citation
--------

If you would like to cite this work, please use the following citation: 

	Esteban-Pérez, A., Morales, J.M. Partition-based distributionally robust optimization via optimal transport with order cone constraints. 4OR-Q J Oper Res (2021). https://doi.org/10.1007/s10288-021-00484-z

You can use this bibtex entry: 

.. code-block:: latex

   @article{Esteban-Pérez2021,
     title={Partition-based distributionally robust optimization via optimal transport with order cone constraints},
     author={Esteban-Pérez, Adrián and Morales, Juan M.}, 
     journal={4OR},
     volume={},
     number={},
     pages={},
     year={2021},
     publisher={Springer}
   

.. _[1]: https://link.springer.com/article/10.1007%2Fs10288-021-00484-z
.. _[2]: https://drive.google.com/uc?export=download&id=1beV5xagcmnoFa1AqZoc1KTsoHJj9BvIi






