# **Artificial Intelligence \(including Machine Learning\)**

> **Prerequisites**: Python \(Anaconda\) + core setup

## **0\) Basic Install**

```
# setup conda envconda create -n aiwork python=3.5 
anaconda sourceactivate aiwork 
conda install -n aiwork -c conda-forge tensorflow=1.0.0 
conda install -n aiwork -c conda-forge jupyter_contrib_nbextensions
```

## **1\) R and RStudio \(other way to install\)**

R is a strong Statistics and ML platform. It gets a huge support from Academia, but extensively used in Industry. Its inclusion in packages make it very easy to import and start using code/ algorithm with ease.

1. Download and Install:[https://cran.r-project.org/bin/macosx/R-3.4.1.pkg](https://cran.r-project.org/bin/macosx/R-3.4.1.pkg)\(for Mac\)

2. Download and install:[https://download1.rstudio.org/RStudio-1.0.153.dmg](https://download1.rstudio.org/RStudio-1.0.153.dmg)\(for Mac \(64bits\)\)

3. Open RStudio

![](https://lh3.googleusercontent.com/COl0dT4M1RHNbnorZolzpHFswSJU8tiMArs3dq7kAePMTpVFufd_NawD0sGVanbVHDiVo-MzoHkTSrcxPx99qn1ieQM6GbU00TS0TTgm46fNVn_AG7NG79hxUmG3-L0iNDutqAxh)

Install some useful packages inside command line in RStudio:

```
install.packages("dplyr")
install.packages("ggraph")
install.packages("igraph")
install.packages("fastICA")
install.packages("ggplot2", lib="/data/Rpackages/")
install.packages("deepnet")
install.packages("caTools")
```

## **2\) DeepLearning \(Theano and Tensorflow\)**

DeepLearn can come in different platforms, and two of the most notable ones are Thano and Tensorflow \(being popular in academia and industry, accordingly\). Both of them are used in python, and their configuration and installation is facilitated via conda.

```
# install Theano
conda install numpy scipy mkl nose sphinx pydot-ng
conda install theano pygpu
```

```
# install TensorFlowconda create -n tensorflowsource activate tensorflow #For python 2.7pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/mac/cpu/tensorflow-1.2.1-py2-none-any.whl#For python 3.4, 3.5, 3.6pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/mac/cpu/tensorflow-1.2.1-py3-none-any.whl pip install --ignore-installed --upgrade \https://storage.googleapis.com/tensorflow/mac/cpu/tensorflow-1.2.1-py2-none-any.whl

```

|  |
| :--- |


**  
**

**Pre-Built Machine Learning Models and Visualization Tools**

**Scikitlearn**

**.**

**  
**

