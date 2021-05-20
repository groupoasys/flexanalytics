.. _FPRPOBVHIO_TPWRS:

Forecasting the Price-response of a Pool of Buildings via Homothetic Inverse Optimization
=========================================================================================
.. sectionauthor:: Asunción Jiménez-Cordero <asuncionjc@uma.es>

This is a summary of the work that can be found in `[1]`_. Open Access pdf is available at `[2]`_

Abstract
--------
This paper focuses on the day-ahead forecasting of the aggregate power of a pool of smart buildings equipped with thermostatically-controlled loads. We first propose the modeling of the aggregate behavior of its power trajectory by using a geometric approach. Specifically, we assume that the aggregate power is a homothet of a prototype building, whose physical and technical parameters are chosen to be the mean of those in the pool. This allows us to preserve the building thermal dynamics of the pool. We then apply inverse optimization to estimate the homothetic parameters with bilevel programming. The lower level characterizes the price-response of the ensemble by a set of marginal utility curves and a homothet of the prototype building, which, in turn, are inferred in the upper-level problem. The upper level minimizes the mean absolute error over a training sample. This bilevel program is transformed into a regularized nonlinear problem that is initialized with the solution given by an efficient heuristic procedure. This heuristic consists in solving two linear programs and its solution is deemed a suitable proxy for the original bilevel problem. The results have been compared to state-of-the-art methodologies.


Citation
--------

If you would like to cite this work, please use the following citation: 

	Ricardo Fernández-Blanco and Juan Miguel Morales and Salvador Pineda, "Forecasting the price-response of a pool of buildings via homothetic inverse optimization" in Applied Energy, vol. 290, pp. 116791, May. 2021

You can use this bibtex entry: 

.. code-block:: latex

  @article{FERNANDEZBLANCO2021116791,
  author={R. {Fernández-Blanco}, J. M. {Morales} and S. {Pineda}},
  journal={Applied Energy}, 
  title={Forecasting the price-response of a pool of buildings via homothetic inverse optimization}, 
  year={2021},
  issn={0306-2619}	
  volume={290},
  pages={116791},}
  

.. _[1]: https://www.sciencedirect.com/science/article/pii/S0306261921002944
.. _[2]: https://drive.google.com/uc?export=download&id=1niryLnkzfxLmH9TgfA6hIjiQJlqZyvlf
