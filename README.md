# fitting-one-term-ogden-model

In the enclosed Jupyter Notebook (``Ogden_Tutorial.ipynb``) we provide a brief tutorial on fitting the one-term Ogden model to an experimental test dataset. The accompanying paper "An Introduction to the Ogden Model in Biomechanics -- Benefits, Implementation Tools, and Limitations" is forthcoming.   

In our tutorial, we are working with a pure shear experimental data. The pure shear testing mode looks like this: 

![PureShear](https://github.com/elejeune11/fitting-one-term-ogden-model/blob/edb472205048280f5d1e324dfb63c67c547a0742/figs/pure_shear.png)

The "homogeneous" approximation of the deformation field can be used to formulate an analytical approximation of an Ogden material undergoing pure shear. The "inhomogeneous" deformation field can be captured by simulating the experimental domain with the finite element method. 

![ExptData](https://github.com/elejeune11/fitting-one-term-ogden-model/blob/f0d8c87234c9dd89c2d5ddf19402e11912a67d5c/figs/expt_test.png)



![Regression](https://github.com/elejeune11/fitting-one-term-ogden-model/blob/f0d8c87234c9dd89c2d5ddf19402e11912a67d5c/figs/fitting_algorithm.png)



![FEA](https://github.com/elejeune11/fitting-one-term-ogden-model/blob/f0d8c87234c9dd89c2d5ddf19402e11912a67d5c/figs/FEA_schematic.png)




![CompareRes](https://github.com/elejeune11/fitting-one-term-ogden-model/blob/f0d8c87234c9dd89c2d5ddf19402e11912a67d5c/figs/fit_comparison.png)
