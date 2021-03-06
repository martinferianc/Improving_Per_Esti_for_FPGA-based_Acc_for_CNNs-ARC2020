# Improving Performance Estimation for FPGA-based Accelerators for Convolutional Neural Networks

A codebase accompanying the paper "Improving Performance Estimation for FPGA-based Accelerators for Convolutional Neural Networks", by Ferianc et al. presented at ARC'2020. The paper is in the repository under [`paper.pdf`](paper.pdf) accompanied by a presentation under [`presentation.pdf`](presentation.pdf). 

1. [Abstract](#Abstract)
2. [Tutorial](#Tutorial)
3. [Requirements](#Requirements)
4. [Running](#Running)
5. [Paper](#Paper)
6. [Citation](#Citation)
7. [Authors](#Authors)
8. [News](#News)

## Abstract

Field-programmable gate array (FPGA) based accelerators are being widely used for acceleration of convolutional neural networks (CNNs) due to their potential in improving the performance and reconfigurability for specific application instances. To determine the optimal configuration of an FPGA-based accelerator, it is necessary to explore the design space and an accurate performance prediction plays an important role during the exploration. This work introduces a novel method for fast and accurate estimation of latency based on a Gaussian process parametrised by an analytic approximation and coupled with runtime data. The experiments conducted on three different CNNs on an FPGA-based accelerator on Intel Arria 10 GX 1150 demonstrated a 30.7% improvement in accuracy with respect to the mean absolute error in comparison to a standard analytic method in leave-one-out cross-validation.

## Tutorial

The tutorial does not involve running and training the estimator on the real data (which is propriatery), it only demonstrates how to build in an analytic mean function that can then later be used inside a a Gaussian process. In order to be able to run the code or build your own estimator follow the steps below.

### Requirements

The requirements to run the code are in `requirements.txt`. The required libraries are:

```
numpy
gpflow<=1.5.1
tensorflow<2.0.0
ipykernel
scipy
sklearn
```

To install them create a virtual environemnt for Python>=3.6 with:

```
virtualenv -p python3 venv
source venv/bin/activate 
```

And install the dependecies with: 

```
pip3 install -r requirements.txt
```

### Running 

Running is just as easy. Make sure that you have insalled all the libraries and then the tutorial is in [`tutorial.ipynb`](tutorial.ipynb). You can run it comfortably in a [Jupyter Notebook](https://jupyter.org/) environment with:

```
jupyter notebook
```

and then navigate to the [`tutorial.ipynb`](tutorial.ipynb) by using the built-in explorer. 

## Paper 

The paper is in the repository under [`paper.pdf`](paper.pdf) accompanied by a presentation under [`presentation.pdf`](presentation.pdf).

## Citation

```
@inproceedings{ferianc2020improving,
  title={Improving Performance Estimation for FPGA-Based Accelerators for Convolutional Neural Networks},
  author={Ferianc, Martin and Fan, Hongxiang and Chu, Ringo SW and Stano, Jakub and Luk, Wayne},
  booktitle={International Symposium on Applied Reconfigurable Computing},
  pages={3--13},
  year={2020},
  organization={Springer}
}
```

## Authors 

Martin Ferianc (martin.ferianc.19@ucl.ac.uk), Hongxiang Fan, Ringo S. W. Chu, Jakub Stano and Wayne Luk, 2020

#### Acknowledgments

We thank Yann Herklotz, Alexander Montgomerie-Corcoran and ARC'20 reviewers for insightful suggestions.

## News 

We were in the news [here](https://www.nextplatform.com/2020/02/24/fpga-inroads-to-convolutional-neural-networks/) and [here](https://www.ucl.ac.uk/electronic-electrical-engineering/news/2020/may/improving-performance-estimation-convolutional-neural-network-accelerators).  
