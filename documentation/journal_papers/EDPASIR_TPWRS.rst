.. _EDPASIR_TPWRS:

An Exact Dynamic Programming Approach to Segmented Isotonic Regression
=======================================================================
.. sectionauthor:: Lisa Huckfield <tradrev12@gmail.com>

This is a summary of the work that can be found in `[1]`_. Open Access pdf is available at `[2]`_.

Abstract
--------

This paper proposes a polynomial-time algorithm to construct the monotone stepwise curve that minimizes the sum of squared errors with respect to a given cloud of data points. The fitted curve is also constrained on the maximum number of steps it can be composed of and on the minimum step length. Our algorithm relies on dynamic programming and is built on the basis that said curve-fitting task can be tackled as a shortest-path type of problem. Numerical results on synthetic and realistic data sets reveal that our algorithm is able to provide the globally optimal monotone stepwise curve fit for samples with thousands of data points in less than a few hours. Furthermore, the algorithm gives a certificate on the optimality gap of any incumbent solution it generates. From a practical standpoint, this piece of research is motivated by the roll-out of smart grids and the increasing role played by the small flexible consumption of electricity in the large-scale integration of renewable energy sources into current power systems. Within this context, our algorithm constitutes an useful tool to generate bidding curves for a pool of small flexible consumers to partake in wholesale electricity markets.


Citation
--------

If you would like to cite this work, please use the following citation: 

	Víctor Bucarey and Martine Labbé and Juan M. Morales and Salvador Pineda, ´An Exact Dynamic Programming Approach to Segmented Isotonic Regression´, `Omega`, vol. , pp. 102516, July 2021.

You can use this bibtex entry: 

.. code-block:: latex

   @article{BUCAREY2021102516,
     title={An exact dynamic programming approach to segmented isotonic regression},
     author={Víctor Bucarey and Martine Labbé and Juan M. Morales and Salvador Pineda},
     journal={Omega},
     volume={},
     number={},
     pages={102516},
     year={2021},
     publisher={Elsevier}
   

.. _[1]: https://www.sciencedirect.com/science/article/pii/S0305048321001250
.. _[2]: https://drive.google.com/uc?export=download&id=10NtLhfcq7pTTJorU0nJKg3K5kNjNRqZn






