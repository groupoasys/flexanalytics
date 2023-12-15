.. _TACSAA_IJOC:

Tight and Compact Sample Average Approximation for Joint Chance Constrained Optimal Power Flow
==============================================================================================
.. sectionauthor:: Lisa Huckfield Morgan <lisa@uma.es>

This is a summary of the work that can be found in `[1]`_. Open Access pdf is available at `[2]`_.

Abstract
--------

In this paper, we tackle the resolution of chance-constrained problems reformulated via Sample Average Approximation. The resulting data-driven deterministic reformulation takes the form of a large-scale mixed-integer program cursed with Big-Ms. We introduce an exact resolution method for the MIP that combines the addition of a set of valid inequalities to tighten the linear relaxation bound with coefficient strengthening and constraint screening algorithms to improve its Big-Ms and considerably reduce its size. The proposed valid inequalities are based on the notion of k-envelopes, can be computed offline using polynomial-time algorithms, and added to the MIP program all at once. Furthermore, they are equally useful to boost the strengthening of the Big-Ms and the screening rate of superfluous constraints. We apply our procedures to a probabilistically-constrained version of the DC Optimal Power Flow problem with uncertain demand. The chance constraint requires that the probability of violating any of the power system's constraints be lower than some parameter ϵ>0. In a series of numerical experiments which involve five power systems of different size, we show the efficiency of the proposed methodology and compare it with some of the best-performing convex inner approximations currently available in the literature. 


Citation
--------

If you would like to cite this work, please use the following citation: 

	Á. Porras, C. Domínguez, J.M. Morales and S. Pineda (2023). Tight and compact sample average approximation for joint chance constrained optimal power flow. INFORMS Journal on Computing, 35(6): 1454--1469.

You can use this bibtex entry: 

.. code-block:: latex

   @article{doi:10.1287/ijoc.2022.0302,
     title={Tight and Compact Sample Average Approximation for Joint Chance-Constrained Problems with Applications to Optimal Power Flow},
     author={Porras, \'{A}lvaro and Dom\'{\i}nguez, Concepci\'{o}n and Morales, Juan Miguel and Pineda, Salvador},
     journal={INFORMS Journal on Computing},
     volume={35},
     number={6},
     pages={1454--1469},
     year={2023},
     publisher={informs PubsOnLine}
   }

.. _[1]: https://pubsonline.informs.org/doi/epdf/10.1287/ijoc.2022.0302
.. _[2]: https://drive.google.com/uc?export=download&id=1D92Yx67XB0YzrY2YukYqt_0JfXo4-FRc






