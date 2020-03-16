.. _DDSNCUC_TPWRS:

Data-Driven Screening of Network Constraints for Unit Commitment
=================================================================
.. sectionauthor:: Asunción Jiménez-Cordero <asuncionjc@uma.es>

This is a summary of the work that can be found in `[1]`_.

Abstract
--------

The transmission-constrained unit commitment (TC-UC) problem is one of the most relevant problems solved by independent system operators for the daily operation of power systems. Given its computational complexity, this problem is usually not solved to global optimality for real-size power systems. In this paper, we propose a data-driven method that leverages historical information to screen out network constraints in the TC-UC problem. First, past data on demand and renewable generation throughout the network are used to learn the congestion status of transmission lines. Then, we infer the lines that will not become congested for upcoming operating conditions based on such learning and disregard their capacity constraints. This way, we formulate a reduced TC-UC problem that is easier to solve. Numerical results on a medium- and a large-size power system show that the proposed approach outperforms existing ones by significantly reducing the computational time while obtaining solutions that are equal or close to the one obtained with the original TC-UC problem. Furthermore, the purely data-driven method we propose can be seamlessly complemented with a constraint generation procedure to guarantee that the optimal solution to the original TC-UC problem is eventually recovered.

Main results
------------
Under construction.

Citation
--------

If you would like to cite this work, please use the following citation: 

	S. Pineda, J. M. Morales, and A. Jiménez-Codero, `Data-Driven Screening of Network Constraints for Unit Commitment`, `IEEE Transactions on Power Systems`, doi:10.1109/TPWRS.2020.2980212, 2020.

You can use this bibtex entry: 

.. code-block:: latex

   @article{pineda2020data,
     title={Data-Driven Network Screening of Network Constraints for Unit Commentment},
     author={Pineda, Salvador and Morales, Juan Miguel and Jim\'enez-Cordero, Asunci\'on},
     journal={IEEE Transactions on Power Systems},
     year={2020},
     doi={10.1109/TPWRS.2020.2980212}, 
   }

.. _[1]: https://ieeexplore.ieee.org/document/9034123


