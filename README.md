## Image Derivatives

A image can be represented as a mapping : $f(x,y)$, in which $(x,y)$ defines coordinates and $f(x,y)$ for intensity value.

We denote the Hessian matrix of $f$ as:

##  $H=\begin{bmatrix}
\dfrac{\partial^{2} f}{\partial x^{2}}&\dfrac{\partial^{2} f}{\partial x \partial y}\\
\dfrac{\partial^{2} f}{\partial x \partial y}&\dfrac{\partial^{2} f}{\partial y^{2}}
\end{bmatrix}$


and we have:
- eigenvalues：$\lambda^{2}-trace(H)+det(H)=0$,  $\lambda=\dfrac{1}{2}\{trace(H) \pm \sqrt{det(H)}\}$

- Laplacian Operator：$\Delta f=trace(H)$