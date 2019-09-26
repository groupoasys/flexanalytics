.. _TAUC_TPWRS:

Time-Adaptive Unit Commitment
=============================
.. sectionauthor:: Salvador Pineda <spinedamorente@gmail.com>

This is a summary of the work that can be found in `[1]`_.

Abstract
--------

The short-term  operation  of a power  system  is  usually planned  by  solving  a  day-ahead  unit  commitment  problem. Due to historical reasons, the commitment of the power generating units is decided over a time horizon typically consisting of the 24 hourly periods of a day. In this paper, we show that, as a result of the increasing  penetration of intermittent renewable generation, this somewhat arbitrary and artificial division of time may prove to be significantly suboptimal and counterproductive. Instead, we propose a time-adaptive day-ahead unit commitment formulation that better captures the net-demand variability throughout the day. The proposed formulation provides the commitment and dispatch of thermal generating units over a set of 24 time periods too, but with different duration. To do that, we use a clustering procedure  to  select  the duration of those adaptive time periods  taking into account the renewable generation and demand forecasts. Numerical results show that, without increasing the computational burden, the proposed time-adaptive unit  commitment  allows  for  a  more  efficient  use  of  the  system flexibility,  which  translates  into  a  lower  operating  cost  and  a higher penetration of renewable production than those achieved by  a  conventional  hourly  unit  commitment  problem.

Main results
------------

Under construction

Citation
--------

If you would like to cite this work, please use the following citation: 

	S. Pineda, R. Fernandez-Blanco, and J. M. Morales, `Time-Adaptive Unit Commitment`, `IEEE Transactions on Power Systems`, vol. 34, no. 5, pp. 3869--3878, Sep. 2019.

You can use this bibtex entry: 

.. code-block:: latex

   @article{pineda2019_tauc,
     title={Time-adaptive unit commitment},
     author={Pineda, Salvador and Fern{\'a}ndez-Blanco, Ricardo and Morales, Juan Miguel},
     journal={IEEE Transactions on Power Systems},
     volume={34},
     number={5},
     pages={3869--3878},
     year={2019},
     publisher={IEEE}
   }


.. _[1]: https://arxiv.org/pdf/1810.00206.pdf







