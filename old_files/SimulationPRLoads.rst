.. _SimulationPRLoads:

Simulation of price-responsive buildings
========================================
.. sectionauthor:: Ricardo Fernández-Blanco <Ricardo.FCarramolino@uma.es>

Smart buildings may respond to price signals by changing consumption patterns. We simulate the behavior of price-responsive households with a floor heating system connected to a ground source based heat pump. Other appliances such as HVAC systems, water heater systems, stove, refrigerator, dishwasher, etc may be taken into account. The goal of this simulation is to provide the consumption of a cluster of buildings that may respond against prices so that their comfort is within desired bounds given external disturbances.  

Mathematical model
------------------

The notation and the formulation are explained next. 

Notation
^^^^^^^^

.. table:: Sets

	=========================== =============================================
	Sets	      				Description
	=========================== =============================================
	:math:`T`     			    Set of time periods
	=========================== =============================================

.. table:: Indices

	============= ===============
	Indices       Description
	============= ===============
	:math:`t`     Index of time periods
	============= ===============

.. table:: Parameters

	==================================== 	===========================================================
	Parameters         	  		      Description
	====================================	===========================================================
	:math:`\boldsymbol{A}`  	      	Matrix of heat-transfer coefficients relating the previous and current states
	:math:`\boldsymbol{B}`  	      	Matrix of coefficients relating the current state with the electricity consumption
	:math:`\boldsymbol{E}`  	      	Matrix of coefficients relating the current state with external disturbances
	:math:`\rho`                            Penalty of slack variables
	:math:`p_{t}`  	      			Electricity price in period :math:`t`
	:math:`x^{max}`  	      			Maximum electricity consumption
	==================================== 	===========================================================

.. table:: Variables

	========================== ===============================================
	Variables                  Description
	========================== ===============================================
	:math:`v_{t}`              Slack variable
	:math:`x_{t}`              Electricity consumption
	:math:`\boldsymbol{y}_t`   Vector of states
 	:math:`\boldsymbol{z}_t`   Vector of external disturbances
	========================== ===============================================

Formulation
^^^^^^^^^^^

The optimization problem for each building follows an Economic Model Predictive Control (EMPC) problem that minimizes the cost of its consumption plus a term for penalizing the discomfort:

.. math::
	\min \sum_{t \in T}{p_{t}x_{t} + \rho v_{t}}
 
	\boldsymbol{y}_t = \boldsymbol{A}\boldsymbol{y}_{t-1}+\boldsymbol{B}x_{t-1}+\boldsymbol{E}\boldsymbol{z}_{t-1}, \forall t \in T

      0 \leq x_{t} \leq x^{max}, \forall t \in T

      y^{r}_{t,min} \leq y^{r}_{t} + v_{t}, \forall t \in T
      
      y^{r}_{t,max} \geq y^{r}_{t} - v_{t}, \forall t \in T
      
      v_{t} \geq 0, \forall t \in T
     
wherein :math:`\boldsymbol{y}_t` is the vector of states :math:`[y_t^r, y_t^f, y_t^w]`, :math:`y_t^r` is the indoor air temperature, :math:`y_t^f` is the floor temperature, :math:`y_t^w` is the temperature of the water inside a tank connected to a heat pump, :math:`\boldsymbol{A}, \boldsymbol{B}, \boldsymbol{E}` are the matrices of the coefficients defining the state-space model, :math:`x_{t}` is the electricity consumption, and :math:`\boldsymbol{z}_{t}` is the vector of external disturbances. The latter vector is made up to two components namely :math:`z_t^a`, which is the outdoor temperature, and :math:`z_t^s`, which is the solar irradiance.


Main results
------------
We compare the two cases analyzed in the `Saez-Gallego's paper`_: 

    * `flex` case: the behavior of 100 buildings (during 2016 hours) is shown when considering comfort bands with two degrees apart from each other. 
    * `noflex` case: the behavior of 100 buildings (during 2016 hours) is shown when considering comfort bands with two degrees apart from each other.
   
To do that, 300 individual simulations were performed by randomly perturbing the heat-transfer coefficients of the matrix :math:`\boldsymbol{A}` of the EMPC model. A uniform distribution centrered around zero with a variance equal to 1/50 the magnitude of the corresponding coefficient was used. 300 building were simulated and the 100 with the least discomfort were chosen in order to avoid unstable solutions.

.. _figure1:
.. figure:: _static/noflexcase_price_vs_load.png
   :width: 100%
   :align: center

   Price and consumption for the `noflex` case

.. _figure2:
.. figure:: _static/flexcase_price_vs_load.png
   :width: 100%
   :align: center

   Price and consumption for the `flex` case


.. _Saez-Gallego's paper: http://ieeexplore.ieee.org/document/7859377/



