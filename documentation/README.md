# Useful tips for developing Sphinx documentation in ReadTheDocs

## Compiling locally

0) We recommend using a python virtual environment: https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/
1) install sphinx: pip install -U sphinx; https://www.sphinx-doc.org/en/master/usage/installation.html
2) open cmd or python console in folder .\flexanalytics\documentation\
3) run: make html
4) the resulting html is in folder .\flexanalytics\documentation\_build
5) navigate to .\flexanalytics\documentation\_build\html an open any .html to see the content in the browser

## Latex syntax  

Including LaTeX equations is simple; http://www.sphinx-doc.org/es/stable/ext/math.html#module-sphinx.ext.imgmath   

.. math::

   (a + b)^2  &=  (a + b)(a + b) \\
              &=  a^2 + 2ab + b^2
              
.. math::
   :nowrap:

   \begin{eqnarray}
      y    & = & ax^2 + bx + c \\
      f(x) & = & x^2 + 2xy + y^2
   \end{eqnarray}
   
.. math:: e^{i\pi} + 1 = 0
   :label: euler

Euler's identity, equation :eq:`euler`, was elected one of the most
beautiful mathematical formulas.
 
IMPORTANT: 
remove \label command
stick to the shown indentation using spaces. 
Leave empty lines surrounding the equations.

## Using Latex locally

Include the following code in the config.py file:

extensions = [  # ... something
                'sphinx.ext.pngmath', 
                # ... something 
                ]

# the documentation of the two following binaries
# those paths works on Windows
pngmath_latex=r"C:\Program Files\MiKTeX 2.9\miktex\bin\x64\latex.exe"
pngmath_dvipng=r"C:\Program Files\MiKTeX 2.9\miktex\bin\x64\dvipng.exe"

You can also rename config_local.py to config.py but remember to revert changes before uploading.
