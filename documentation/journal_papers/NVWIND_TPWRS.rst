.. _NVWIND_TPWRS:

Feature-driven Improvement of Renewable Energy Forecasting and Trading
======================================================================
.. sectionauthor:: Miguel Angel Muñoz <miguelangeljmd@uma.es>

This is a summary of the work that can be found in `[1]`_. Open Access pdf is available at `[2]`_

Abstract
--------

Inspired from recent insights into the common ground of machine learning, optimization and decision-making, this paper proposes an easy-to-implement, but effective procedure to enhance both the quality of renewable energy forecasts and the competitive edge of renewable energy producers in electricity markets with a dual-price settlement of imbalances. The quality and economic gains brought by the proposed procedure essentially stem from the utilization of valuable predictors (also known as features) in a data-driven newsvendor model that renders a computationally inexpensive linear program. We illustrate the proposed procedure and numerically assess its benefits on a realistic case study that considers the aggregate wind power production in the Danish DK1 bidding zone as the variable to be predicted and traded. Within this context, our procedure leverages, among others, spatial information in the form of wind power forecasts issued by transmission system operators (TSO) in surrounding bidding zones and publicly available in online platforms. We show that our method is able to improve the quality of the wind power forecast issued by the Danish TSO by several percentage points (when measured in terms of the mean absolute or the root mean square error) and to significantly reduce the balancing costs incurred by the wind power producer.

Main results
------------

The optimal offer :math:`{E}^{D}` that a (price-taker) risk-neutral renewable energy producer should place in the day-ahead market is given as the solution to the following linear programming problem, whereby the renewable energy producer seeks to minimize the expected opportunity cost for under- and overproduction

.. math::
   :nowrap:

   \begin{align*}
       \min_{E^D \in [0, \overline{E}]}   \mathbb{E}\left[\psi^{-}(E^D - E)^{+} + \psi^{+}(E - E^D)^{+}\right]
   \end{align*}

where :math:`(x)^{+}:= \max(x,0)`, :math:`E^{D}`, :math:`E`, :math:`\psi^{-}` and :math:`\psi^{+}` represent the day-ahead renewable energy bid, the eventual renewable energy production, the marginal opportunity costs for under- and overproduction, respectively. We propose to work with the enriched dataset :math:`\{(E_t, \psi_t^{-}, \psi_t^{+}, {x}_t), \forall t \in \boldsymbol{T} \}`, where :math:`x` represents a vector of available auxiliary information and the subscript :math:`t` represents that the sample was observed at time t. We take advantage of the available auxiliary information introducing in the model the following linear decision rule:

.. math::
   :nowrap:
   
   \begin{align*}
       \mathcal{Q}=\Big \{ E^D: \mathcal{X} \to \mathbb{R}:E^D(x) = \mathbf{q \cdot x} = \sum_{j=1}^p q^j x^j \Big \},
   \end{align*}


We developed a general optimization framework to improve renewable energy forecasting and trading that translates into a two-step optimization procedure. We first obtain an improved forecast using auxiliary information, such as, renewable energy forecast of nearby areas. The second optimization problem accepts this enhanced forecast and produces an optimal offer considering the past under- and overproduction costs. The general framework is given by:

.. math::
   :nowrap:

   \begin{align*}
       &\min_{\mathbf{q}} \frac{1}{|\mathcal{T}|} \sum_{t\in\mathcal{T}} \psi_t^{-}\left(\sum_{j=1}^p q^j x^j_t - E_t\right)^{+}\! +\! \psi_t^{+}\left(E_t - \sum_{j=1}^p q^j x^j_t\right)^{+}\\
       & \text{s. t.}  0 \leq \sum_{j=1}^p q^j x^j_t \leq \overline{E},  \forall t\in\mathcal{T}
   \end{align*}


To recast the previous framework as a linear program tailored to forecasting, we introduce the auxiliary variables :math:`o_t` and :math:`u_t` and set :math:`\psi_t^{+}` and :math:`\psi_t^{-}` to one. The forecasting model of the first step results as follows:

.. math::
   :nowrap:

   \begin{align*}
       &\min_{\mathbf{q}, \mathbf{u}, \mathbf{o}} \quad \frac{1}{|\mathcal{T}|} \sum_{t\in\mathcal{T}} u_t + o_t\\
       &\text{s. t.}  u_t \geq \sum_{j=1}^p q^j x^j_t - E_t,  \forall t\in\mathcal{T}\\
       & \phantom{s. t.}  o_t \geq E_t - \sum_{j=1}^p q^j x^j_t,  \forall t\in\mathcal{T}\\
       & \phantom{s. t.}  0 \leq \sum_{j=1}^p q^j x_t^j \leq \overline{E},  \forall t\in\mathcal{T}\\
       & \phantom{s. t.}  u_t, o_t \geq 0,  \forall t\in\mathcal{T} 
   \end{align*}


The second optimization problem is a single feature model, where, :math:`\hat{w}`, represents the improved renewable energy forecast obtained from the first step. This second step adapts the input values based on mid-term patterns that may be found in deviation costs. The model is formulated as follows:

.. math::
   :nowrap:

   \begin{align*}
       &\min_{a, \mathbf{u}, \mathbf{o}} \quad \frac{1}{|\mathcal{T}|} \sum_{t\in\mathcal{T}} \psi_t^{-}u_t + \psi_t^{+}o_t\\
       &\text{s. t.}  u_t \geq a \hat{w}_t - E_t,  \forall t \in \mathcal{T}\\
       & \phantom{s. t.}  o_t \geq E_t - a \hat{w}_t,  \forall t \in \mathcal{T}\\
       & \phantom{s. t.}  u_t, o_t \geq 0,  \forall t \in \mathcal{T}
   \end{align*}

We elaborate several realistic models with actual TSO data from 01/08/2015 to 04/22/2019, freely accesible at the ENTSO-e Tranparency Platform that we train following a realistic rolling window procedure. As a result, we are able to improve the DK1 onshore wind power forecast delivered by the danish TSO, both for forecasting and trading. Following this procedure, we report an average 8.53% MAE improvement and 2.13% opportunity cost reduction over the test period.

Citation
--------

If you would like to cite this work, please use the following citation: 

	M. A. Muñoz, J. M. Morales, and S. Pineda, `Feature-driven Improvement of Renewable Energy Forecasting and Trading`, `IEEE Transactions on Power Systems`, vol. n/a, no. n/a, pp. n/a, n/a 2020.

You can use this bibtex entry: 

.. code-block:: latex

   @article{Munoz2019feat,
     title={Feature-driven Improvement of Renewable Energy Forecasting and Trading},
     author={Mu{\~n}oz, Miguel Angel and Morales, Juan Miguel and Pineda, Salvador},
     journal={IEEE Transactions on Power Systems},
     year={2020},
     volume={}, 
     number={}, 
     pages={},
     publisher={IEEE},
     keywords={Electricity markets; Machine Learning; Optimization; Renewable energy forecasting and trading; Windpower},
     doi={10.1109/TPWRS.2020.2975246}, 
   }



.. _[1]: https://www.doi.org/10.1109/TPWRS.2020.2975246
.. _[2]: https://drive.google.com/uc?export=download&id=10fnLcyWm0dAu82dyem9ITJT4ZOxSiJ0P

.. This is a comment: https://ieeexplore.ieee.org/document/10.1109/TPWRS.2020.2975246






