.. _DDSNCUC_TPWRS:

Data-Driven Screening of Network Constraints for Unit Commitment
=================================================================
.. sectionauthor:: Asunción Jiménez-Cordero <asuncionjc@uma.es>

This is a summary of the work that can be found in `[1]`_. Open Access pdf is available at `[2]`_

Abstract
--------

The transmission-constrained unit commitment (TC-UC) problem is one of the most relevant problems solved by independent system operators for the daily operation of power systems. Given its computational complexity, this problem is usually not solved to global optimality for real-size power systems. In this paper, we propose a data-driven method that leverages historical information to screen out network constraints in the TC-UC problem. First, past data on demand and renewable generation throughout the network are used to learn the congestion status of transmission lines. Then, we infer the lines that will not become congested for upcoming operating conditions based on such learning and disregard their capacity constraints. This way, we formulate a reduced TC-UC problem that is easier to solve. Numerical results on a medium- and a large-size power system show that the proposed approach outperforms existing ones by significantly reducing the computational time while obtaining solutions that are equal or close to the one obtained with the original TC-UC problem. Furthermore, the purely data-driven method we propose can be seamlessly complemented with a constraint generation procedure to guarantee that the optimal solution to the original TC-UC problem is eventually recovered.

Main results
------------
Reducing the computational burden of the TC-UC problem is a very relevant research topic within the PES community. One approach to address this issue consists in disregarding the capacity constraints of those transmission lines that will not become active during operation. Although there are some existing works in this direction, most of them focus on removing redundant network constraints in order not to alter the original feasible region of the TC-UC problem.

In this paper, we propose a data-driven approach that takes advantage of historical information to disregard both redundant and inactive network constraints. In doing so, we remove a larger number of network constraints than existing methods and achieve higher computational savings, which range from 70% to 98% depending on the congestion level of the power system and its size. As a counterpart, the proposed approach yields commitment decisions that may be slightly different from those obtained by the original TC-UC problem. If required, such small inaccuracies can be completely eliminated by running a post-processing step based on a constraint generation procedure to recover the solution to the original TC-UC problem.


Citation
--------

If you would like to cite this work, please use the following citation: 

	S. Pineda, J. M. Morales and A. Jiménez-Cordero, "Data-Driven Screening of Network Constraints for Unit Commitment," in IEEE Transactions on Power Systems, vol. 35, no. 5, pp. 3695-3705, Sept. 2020.

You can use this bibtex entry: 

.. code-block:: latex

  @ARTICLE{9034123,
  author={S. {Pineda} and J. M. {Morales} and A. {Jiménez-Cordero}},
  journal={IEEE Transactions on Power Systems}, 
  title={Data-Driven Screening of Network Constraints for Unit Commitment}, 
  year={2020},
  volume={35},
  number={5},
  pages={3695-3705},}

.. _[1]: https://ieeexplore.ieee.org/document/9034123
.. _[2]: https://drive.google.com/file/d/1VehrTy1EGHBFxEwCHkSBQo---c7tGIM5/view?usp=sharing

