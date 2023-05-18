# Project-2--Linear
Numerical Methods Project 2 - Linear Algebra

This repository contains a Julia notebook which approximates the $\sin(x)$ function and quantifies the errors of the approximation. It also explores how to take derivatives of our polynomial approximation of our functions. This can be ran as any other notebook on a machine capable of executing Julia code. 

## 1)

We start by studying our polynomial approximation to the $\sin(x)$ funciton. When approximated with a degree 10 polynomial we see strong aggreement with our approximated function and the actual function. 

![sinapprox](https://github.com/ColeLovesSpace/Project-2--Linear/assets/122398597/cad0d7b3-de10-4064-b032-0323cd37c370)

Both the actual function and the approximated function are plotted here but it looks as though there is only one line. 

## 2)

Next we quantify the errors in our approximation by caculating the L2 norm as a function of the degree of our polynomial approximation. 

![errorVsDeg](https://github.com/ColeLovesSpace/Project-2--Linear/assets/122398597/fe7bd253-b781-489f-98fe-c57608ef0012)

Here we see that it takes a degree 9 polynomial to reach the desired error in our function, but the error increases with the degree beyond that which is interesting. We are unable to reach a lower error with our approximation due to the intrisic error of floating point operations. 

## 3)

Here we use a strictly antisymetric polynomial to approximate our odd function. This amounts to only using the odd degrees of our polynomial which saves on the computation neccisary to approximate the function. Here we plot the error as a function of computational cost in terms of the number of coefficients used to approximate the function.

![errorVsCost](https://github.com/ColeLovesSpace/Project-2--Linear/assets/122398597/c4397e42-206d-4188-b5fc-bdf7b318ecef)

We can see that our antisymmetric approximation reaches the desired error faster than our general polynomial approximation, meaning that we can save computational resourses by understanding the function we are approximating and what is neccisary to reproduce it. 

## 4)

Now we calculate the derivitive of our approximation manually by differentiating the polynomial, and we also numerically calculate the coefficients of our derivative function to compare them. Both are able to reliably reproduce the cosine function as seen in the plot below. 

![approxDeriv](https://github.com/ColeLovesSpace/Project-2--Linear/assets/122398597/e6f87188-2592-48f8-8cf4-dde8b4fa5d21)

