# Image Derivative (Part 1)

## Theory

An image can be represented as a mapping : *f(x,y)*, in which *(x,y)* defines coordinates and *f(x,y)* for intensity value.

### First- and Second Order Derivative

![deri1](https://github.com/qinhaihong-red/image_derivatives/raw/master/images/deri1.png)

![deri2](https://github.com/qinhaihong-red/image_derivatives/raw/master/images/deri2.png)

### Hessian Matrix

We can denote the Hessian matrix ,which is based on the second derivative talked above, of *f* as:
![hess](https://github.com/qinhaihong-red/image_derivatives/raw/master/images/hess.png)

Hessian matrix is usefull when applied in feature detection such as corners and edges.


# Practise

In practise, we usaully convolve the image with specified kernels such as Sobel kernel to approximate the derivative talked above.

Let's see how these kernels look like and we will use OpenCV to illustrate this.

Sobel first order kernel for first order derivative approximation in x direction:

```
x,y=cv2.getDerivKernels(1,0,3)
kx1=y*x.transpose()
print(kx1)
```
![kx1](https://github.com/qinhaihong-red/image_derivatives/raw/master/images/kx1.png)

second order kernel in x direction:
```
x,y=cv2.getDerivKernels(2,0,3)
kx2=y*x.transpose()
print(kx2)
```
![kx2](https://github.com/qinhaihong-red/image_derivatives/raw/master/images/kx2.png)

and the mixed partial:
```
x,y=cv2.getDerivKernels(1,1,3)
kxy=y*x.transpose()
print(kxy)
```
![kxy](https://github.com/qinhaihong-red/image_derivatives/raw/master/images/kxy.png)



You can get the kernel for $y$ in the same way.