.. _IOKRAPFBFEV_TPWRS:

Inverse Optimization with Kernel Regression: Application to The Power Forecasting and Bidding Of A Fleet Of Electric Vehicles
===========================================================================================================
.. sectionauthor:: Lisa Huckfield <tradrev12@gmail.com>

This is a summary of the work that can be found in `[1]`_. Open Access pdf is available at `[2]`_.

Abstract
--------

This paper considers an aggregator of Electric Vehicles (EVs) who aims to learn the aggregate power of his/her fleet while also participating in the electricity market. The proposed approach is based on a data-driven inverse optimization (IO) method, which is highly nonlinear. To overcome such a caveat, we use a two-step estimation procedure which requires solving two convex programs. Both programs depend on penalty parameters that can be adjusted by using grid search. In addition, we propose the use of kernel regression to account for the nonlinear relationship between the behavior of the pool of EVs and the explanatory variables, i.e., the past electricity prices and EV fleet’s driving patterns. Unlike any other forecasting method, the proposed IO framework also allows the aggregator to derive a bid/offer curve, i.e. the tuple of price-quantity to be submitted to the electricity market, according to the market rules. We show the benefits of the proposed method against the machine-learning techniques that are reported to exhibit the best forecasting performance for this application in the technical literature.


Citation
--------

If you would like to cite this work, please use the following citation: 

	R. Fernández-Blanco, J. M. Morales, S. Pineda, and Á. Porras ´Inverse Optimization with Kernel Regression: Application to The Power Forecasting and Bidding Of A Fleet Of Electric Vehicles´, `Computer and Operations Research`, vol. 134, pp. 105405, Oct. 2021.

You can use this bibtex entry: 

.. code-block:: latex

   @article{FERNANDEZBLANCO2021105405,
     title={Inverse optimization with kernel regression: Application to the power forecasting and bidding of a fleet of electric vehicles},
     author={Ricardo Fernández-Blanco and Juan Miguel Morales and Salvador Pineda and Álvaro Porras},
     journal={Computers & Operations Research},
     volume={134},
     number={},
     pages={105405},
     year={2021},
     publisher={Elsevier}
   }

.. _[1]: https://www.sciencedirect.com/science/article/pii/S0305054821001696?via%3Dihub
.. _[2]: https://drive.google.com/uc?export=download&id=1UwSKDimDY0To_2s0SwAEyTWLhMbMLFQ1






