.. _WSCGMIO_KBS:

Warm-starting Constraint Generation for Mixed-integer Optimization: A Machine Learning Approach
===============================================================================================
.. sectionauthor:: Lisa Huckfield

This is a summary of the work that can be found in `[1]`_. Open Access pdf is available at `[2]`_.

Abstract
--------
Mixed Integer Linear Programs (MILP) are well known to be NP-hard (Non-deterministic Polynomial-time hard) problems in general. Even though pure optimization-based methods, such as constraint generation, are guaranteed to provide an optimal solution if enough time is given, their use in online applications remains a great challenge due to their usual excessive time requirements. To alleviate their computational burden, some machine learning techniques (ML) have been proposed in the literature, using the information provided by previously solved MILP instances. Unfortunately, these techniques report a non-negligible percentage of infeasible or suboptimal instances. By linking mathematical optimization and machine learning, this paper proposes a novel approach that speeds up the traditional constraint generation method, preserving feasibility and optimality guarantees. In particular, we first identify offline the so-called invariant constraint set of past MILP instances. We then train (also offline) a machine learning method to learn an invariant constraint set as a function of the problem parameters of each instance. Next, we predict online an invariant constraint set of the new unseen MILP application and use it to initialize the constraint generation method. This warm-started strategy significantly reduces the number of iterations to reach optimality, and therefore, the computational burden to solve online each MILP problem is significantly reduced. Very importantly, all the feasibility and optimality theoretical guarantees of the traditional constraint generation method are inherited by our proposed methodology. The computational performance of the proposed approach is quantified through synthetic and real-life MILP applications.


Citation
--------

If you would like to cite this work, please use the following citation: 

	Asunción Jiménez-Cordero, Juan Miguel Morales, Salvador Pineda `Warm-starting Constraint Generation for Mixed-integer Optimization: A Machine Learning Approach` in Knowledge-Based Systems vol. 253 pp. 109570, 2022.

You can use this bibtex entry: 

.. code-block:: latex

  @ARTICLE{JIMENEZCORDERO2022109570,
  author={{Asunción Jiménez-Cordero and Juan Miguel Morales and Salvador Pineda}},  
  journal={Knowledge-Based Systems},   
  title={Warm-starting constraint generation for mixed-integer optimization: A Machine Learning Approach},  
  year={2022},  
  volume={253},  
  number={-},  
  pages={109570},  
  doi={10.1016/j.knosys.2022.109570}}
  ISSN={0950-7051},}

.. _[1]: https://www.sciencedirect.com/science/article/pii/S0950705122007894
.. _[2]: https://riuma.uma.es/xmlui/handle/10630/24887

