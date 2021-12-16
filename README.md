# A Tutorial on Fitting the One-Term Ogden Model

In the enclosed Jupyter Notebook (``Ogden_Tutorial.ipynb``) we provide a brief tutorial on fitting the one-term Ogden model to an experimental test dataset. The accompanying paper "An Introduction to the Ogden Model in Biomechanics -- Benefits, Implementation Tools, and Limitations" is forthcoming.   

In our tutorial, we are working with pure shear experimental data. The pure shear testing mode looks like this: 

![PureShear](https://github.com/elejeune11/fitting-one-term-ogden-model/blob/edb472205048280f5d1e324dfb63c67c547a0742/figs/pure_shear.png)

The "homogeneous" approximation of the deformation field can be used to formulate an analytical approximation of an Ogden material undergoing pure shear. The "inhomogeneous" deformation field can be captured by simulating the experimental domain with the finite element method. In this tutorial, we work with experimental test data performed on blood clot coagulated in vitro. For more information on this material, please see [1,2,3]. For our example, the experimental data looks like this: 

![ExptData](https://github.com/elejeune11/fitting-one-term-ogden-model/blob/f0d8c87234c9dd89c2d5ddf19402e11912a67d5c/figs/expt_test.png)

In our tutorial, we provide code to fit this experimental data to the one-term Ogden model using the ``scipy.optimize.curve_fit'' function. First, we demonstrate this process with the analytical solution implemented as a simple Python function. Then, we demonstrate this process with finite element forward simulations run in FEBio []. The basic algorithm looks like this: 

![Regression](https://github.com/elejeune11/fitting-one-term-ogden-model/blob/f0d8c87234c9dd89c2d5ddf19402e11912a67d5c/figs/fitting_algorithm.png)

To obtain the finite element solution, we call the finite element software FEBio from a Python function. For this code to run, you will need to download the FEBio executable from: <https://febio.org/>. For efficiency, we only simulate 1/8th of the domain: 

![FEA](https://github.com/elejeune11/fitting-one-term-ogden-model/blob/f0d8c87234c9dd89c2d5ddf19402e11912a67d5c/figs/FEA_schematic.png)

For this example, both the analytical solution and the finite element solution fit the experimental data quite well:

![CompareRes](https://github.com/elejeune11/fitting-one-term-ogden-model/blob/f0d8c87234c9dd89c2d5ddf19402e11912a67d5c/figs/fit_comparison.png)

We hope that you find this tutorial useful!

# References
