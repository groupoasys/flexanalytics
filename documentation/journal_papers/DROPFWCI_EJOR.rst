.. _DROPFWCI_EJOR:

Distributionally Robust Optimal Power Flow with Contextual Information
======================================================================
.. sectionauthor:: Lisa Huckfield

This is a summary of the work that can be found in `[1]`_. Open Access pdf is available at `[2]`_.

Abstract
--------
In this paper, we develop a distributionally robust chance-constrained formulation of the Optimal Power Flow problem (OPF) whereby the system operator can leverage contextual information. For this purpose, we exploit an ambiguity set based on probability trimmings and optimal transport through which the dispatch solution is protected against the incomplete knowledge of the relationship between the OPF uncertainties and the context that is conveyed by a sample of their joint probability distribution. We provide a tractable reformulation of the proposed distributionally robust chance-constrained OPF problem under the popular conditional-value-at-risk approximation. By way of numerical experiments run on a modified IEEE-118 bus network with wind uncertainty, we show how the power system can substantially benefit from taking into account the well-known statistical dependence between the point forecast of wind power outputs and its associated prediction error. Furthermore, the experiments conducted also reveal that the distributional robustness conferred on the OPF solution by our probability-trimmings-based approach is superior to that bestowed by alternative approaches in terms of expected cost and system reliability.


Citation
--------

If you would like to cite this work, please use the following citation: 

	Adrián Esteban-Pérez, Juan M. Morales, ´Distributionally Robust Optimal Power Flow with Contextual Information` European Journal of Operational Research, 2022

You can use this bibtex entry: 

.. code-block:: latex

  @article{ESTEBANPEREZ2022,
title = {Distributionally Robust Optimal Power Flow with Contextual Information},
journal = {European Journal of Operational Research},
year = {2022},
issn = {0377-2217},
doi = {https://doi.org/10.1016/j.ejor.2022.10.024},
url = {https://www.sciencedirect.com/science/article/pii/S0377221722008128},
author = {Adrián Esteban-Pérez and Juan M. Morales},
}

.. _[1]: https://www.sciencedirect.com/science/article/pii/S0377221722008128
.. _[2]: https://arxiv.org/abs/2109.07896
