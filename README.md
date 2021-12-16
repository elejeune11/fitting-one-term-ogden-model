# A Tutorial on Fitting the One-Term Ogden Model

In the enclosed Jupyter Notebook ``Ogden_Tutorial.ipynb`` we provide a brief tutorial on fitting the one-term Ogden model to an experimental test dataset. The accompanying paper "An Introduction to the Ogden Model in Biomechanics -- Benefits, Implementation Tools, and Limitations" is forthcoming.   

In our tutorial, we are working with pure shear experimental data. The pure shear testing mode looks like this: 

<p align="center">
<img src="https://github.com/elejeune11/fitting-one-term-ogden-model/blob/edb472205048280f5d1e324dfb63c67c547a0742/figs/pure_shear.png" width="600">
</p>

\

The "homogeneous" approximation of the deformation field can be used to formulate an analytical approximation of an Ogden material undergoing pure shear. The "inhomogeneous" deformation field can be captured by simulating the experimental domain with the finite element method. In this tutorial, we work with experimental test data performed on blood clot coagulated in vitro. For more information on blood clot, please see [1,2]. For our example, the experimental data looks like this: 

<p align="center">
<img src="https://github.com/elejeune11/fitting-one-term-ogden-model/blob/f0d8c87234c9dd89c2d5ddf19402e11912a67d5c/figs/expt_test.png" width="600">
</p>

\

In our tutorial, we provide code to fit this experimental data to the one-term Ogden model using the ``scipy.optimize.curve_fit`` function. First, we demonstrate this process with the analytical solution implemented as a simple Python function. Then, we demonstrate this process with finite element forward simulations run in FEBio [3]. The basic algorithm looks like this: 

<p align="center">
<img src="https://github.com/elejeune11/fitting-one-term-ogden-model/blob/f0d8c87234c9dd89c2d5ddf19402e11912a67d5c/figs/fitting_algorithm.png" width="500">
</p>

\

To obtain the finite element solution, we call the finite element software FEBio from a Python function. For this code to run, you will need to download the FEBio executable from: <https://febio.org/>. For efficiency, we only simulate 1/8th of the domain: 

<p align="center">
<img src="https://github.com/elejeune11/fitting-one-term-ogden-model/blob/f0d8c87234c9dd89c2d5ddf19402e11912a67d5c/figs/FEA_schematic.png" width="600">
</p>

\

For this example, both the analytical solution and the finite element solution fit the experimental data quite well:

<p align="center">
<img src="https://github.com/elejeune11/fitting-one-term-ogden-model/blob/f0d8c87234c9dd89c2d5ddf19402e11912a67d5c/figs/fit_comparison.png" width="600">
</p>

\

We hope that you find the tutorial useful!

# References

1. Sugerman, G. P., Chokshi, A., & Rausch, M. K. (2021). Preparation and Mounting of Whole Blood Clot Samples for Mechanical Testing. Current Protocols, 1(7), e197. <https://currentprotocols.onlinelibrary.wiley.com/doi/abs/10.1002/cpz1.197>
2. Sugerman, G. P., Kakaletsis, S., Thakkar, P., Chokshi, A., Parekh, S. H., & Rausch, M. K. (2021). A whole blood thrombus mimic: Constitutive behavior under simple shear. Journal of the Mechanical Behavior of Biomedical Materials, 115, 104216. <https://www.sciencedirect.com/science/article/pii/S1751616120307566>
3. Maas, S. A., Ellis, B. J., Ateshian, G. A., & Weiss, J. A. (2012). FEBio: finite elements for biomechanics. Journal of biomechanical engineering, 134(1). <https://doi.org/10.1115/1.4005694>
