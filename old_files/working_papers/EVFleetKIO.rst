.. _EVFleetKIO:

EV-Fleet Power Forecasting via Kernel-Based Inverse Optimization
================================================================
.. sectionauthor:: Ricardo Fern\'andez-Blanco <Ricardo.FCarramolino@uma.es>

This is a summary of the work that can be found in `[1]`_.

Abstract
--------
This work considers an aggregator of Electric Vehicles (EVs) who aims to forecast the aggregate power of her fleet. The forecasting approach is based on a data-driven inverse optimization (IO) method, which is highly nonlinear. To overcome such a caveat, we use a two-step estimation procedure which requires to solve two convex programs. Both programs depend on penalty parameters that can be adjusted by using grid search. In addition, we propose the use of kernel regression to account for the nonlinear relationship between the behaviour of the pool of EVs and the explanatory variables, i.e., the past electricity prices and EV fleet's driving patterns. Unlike any other forecasting method, the proposed IO framework also allows the aggregator to derive a bidding curve, i.e. the tuple of price-quantity to be submitted to the electricity market, according to the market rules. We show the effective performance of the proposed method against state-of-the-art machine-learning techniques.

Main results
------------

We assume a residential aggregator with 100 EVs and that the EVs do not enable their V2G capabilities. We compare the results for three cases: 

	* `naive-ch` case: The EVs satisfy their energy needs by using a naive charging. In this case each EV will be charged to its required maximum energy as soon as it is available, thus neglecting the dependence of the charging power on the price.
	* `sync` case: The charging is highly synchronized.
	* `non-sync` case: The charging synchronization is avoided.

Note that the cases `sync` and `non-sync` are driven by the cost minimization of the EV's aggregator wherein the electricity prices are accounted for. 

The sizes of the training, validation, and test sets are 672 h, 168 h, and 168 h, in that order. :numref:`fig_kio1` represents the hourly electricity price versus the corresponding charging power for all periods of the training set for the cases mentioned above. As can be seen, the aggregate power of the `non-sync` case depends linearly on the price, unlike cases `naive-ch` and `sync`.

.. _fig_kio1:
.. figure:: img/power_price_g2v_coloured.png
   :width: 100%
   :align: center

   Power versus price for cases (a) `naive-ch`, (b) `sync`, and (c) `non-sync`

Apart from the improvement in terms of RMSE (root mean square error) and MAE (mean absolute error) of the proposed approach `kio` against the rest of the models to forecast the EV-fleet power, `kio` is able to provide a bidding curve, as imposed by rules in electricity markets. :numref:`fig_kio2`, :numref:`fig_kio3`, and :numref:`fig_kio4` show the results for cases `naive-ch`, `sync`, and `non-sync`, respectively. In the upper plots of :numref:`fig_kio3` and :numref:`fig_kio4`, we show the estimated marginal utility prices for the six blocks for each hour of the first day of the test set and for the cases `sync` and `non-sync`. Correspondingly, :numref:`fig_kio2` and the lower plots of :numref:`fig_kio3` and :numref:`fig_kio4` depict the estimated bounds as well as the forecast and observed EV-fleet power for such a day. 

In the `naive-ch` case, the `kio` provides coincident power bounds, as illustrated in :numref:`fig_kio2`, which means that the optimality problem (i.e. the marginal utility estimation problem, which captures the price effect) is useless and thus the aggregate charging power can be directly explained by estimating the bounds. In the upper plots of :numref:`fig_kio3` and :numref:`fig_kio4`, we can observe that the `kio` model identifies whether the EV-fleet power is price-responsive or not by assigning different values to the marginal utility for each block. On the one hand, in :numref:`fig_kio3`, the blockwise marginal utilities are almost identical at any time period, thus suggesting that the EV fleet is almost inelastic for the `sync` case. In this case, the power bounds are basically shaping the EV-fleet charging forecast. On the other hand, for the `non-sync` case, the bounds are generally wider than those obtained for the `sync` case (see :numref:`fig_kio4`). The marginal utility is thus shaping the aggregate power forecast since the `kio` model gives rise to a wider range of marginal utility values at any time period, as can be observed in :numref:`fig_kio4`. In short, unlike any other forecasting tool, we gain interpretability with the proposed inverse optimization approach `kio` due to two aspects: (i) the width of the bounds, which sheds light on the price-responsiveness of the EV fleet; and (ii) the derivation of a bidding curve when there exists a dependence of the EV-fleet power on the price.


.. _fig_kio2:
.. figure:: img/case_g2v_naive_coloured.png
   :width: 100%
   :align: center

   Estimated power bounds as well as forecast and observed power for case `naive-ch`

.. _fig_kio3:
.. figure:: img/case_g2v_a0_coloured.png
   :width: 100%
   :align: center

   Results for case `sync`: (a) Estimated marginal utility price per block and electricity price, and (b) estimated power bounds as well as forecast and observed power. Note that the inset plot represents the bid price function and the corresponding electricity price of hour 5

.. _fig_kio4:
.. figure:: img/case_g2v_anot0_coloured.png
   :width: 100%
   :align: center

   Results for case `non-sync`: (a) Estimated marginal utility price per block and electricity price, and (b) estimated power bounds as well as forecast and observed power. Note that the inset plot represents the bid price function and the corresponding electricity price of hour 5

If you would like to know more about this work, you can read it in `[1]`_.


.. _[1]: https://arxiv.org/pdf/1908.00399.pdf







