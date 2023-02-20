.. _CDCNSFUCP_TPWRS:

Cost-driven Screening of Network Constraints for the Unit Commitment Problem
============================================================================
.. sectionauthor:: Lisa Huckfield

This is a summary of the work that can be found in `[1]`_. Open Access pdf is available at `[2]`_.

Abstract
--------

In an attempt to speed up the solution of the unit commitment (UC) problem, both machine-learning and optimization-based methods have been proposed to lighten the full UC formulation by removing as many superfluous line-flow constraints as possible. While the elimination strategies based on machine learning are fast and typically delete more constraints, they may be over-optimistic and result in infeasible UC solutions. For their part, optimization-based methods seek to identify redundant constraints in the full UC formulation by exploring the feasibility region of an LP-relaxation. In doing so, these methods only get rid of line-flow constraints whose removal leaves the feasibility region of the original UC problem unchanged. In this paper, we propose a procedure to substantially increase the line-flow constraints that are filtered out by optimization-based methods without jeopardizing their appealing ability of preserving feasibility. Our approach is based on tightening the LP-relaxation that the optimization-based method uses with a valid inequality related to the objective function of the UC problem and hence, of an economic nature. The result is that the so strengthened optimization-based method identifies not only redundant line-flow constraints but also inactive ones, thus leading to more reduced UC formulations.


Citation
--------

If you would like to cite this work, please use the following citation: 

	A. Porras, S. Pineda, J. M. Morales and A. Jimenez-Cordero, "Cost-driven Screening of Network Constraints for the Unit Commitment Problem," in IEEE Transactions on Power Systems, vol. 38, no. 1, pp. 42-51, Jan. 2023.

Alternatively you could use this bibtex entry: 

.. code-block:: latex

  @ARTICLE{9736690,
  author={{Porras, Alvaro and Pineda, Salvador and Morales, Juan Miguel and Jimenez-Cordero, Asuncion}},  
  journal={IEEE Transactions on Power Systems},   
  title={Cost-driven Screening of Network Constraints for the Unit Commitment Problem},  
  year={2023},  
  volume={38},  
  number={1},  
  pages={42-51},  
  doi={10.1109/TPWRS.2022.3160016}}
  ISSN={1558-0679},}

.. _[1]: https://ieeexplore.ieee.org/document/9736690/authors#authors
.. _[2]: https://drive.google.com/uc?export=download&id=1gJ7FG3l_Tsr6g-2xVerC4MD0bL93fmGw 


