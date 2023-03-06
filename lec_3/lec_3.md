## $${Lecture \space 3}$$  
### ${\color{red}Notes}$  
* always label your graphs  
* calculations so far depend on the basics of differentiation &rarr; not the only way  
* always get back to first principles  
* the derivative gets distributed over the summation &rarr; almost like an operator getting distributed  
* ***local gradient*** &rarr; partial derivative with respect to its immediate input  
* ***back propagation*** *(chain rule)* is the optimal/main algorithm for implementation of neural networks  

* $${\dfrac{\partial L}{\partial x_p} = - \dfrac{1}{N} \sum_{i=0}^{N-1} ((x_i - x_p)^2 + (y_i - y_p)^2)^{-\frac{1}{2}} (x_i - x_p)}$$  

* calculate derivative mathematically in a closed form  
* chain rule &rarr; traverse recursively backwards  
* instead of creating a list and using a sum function we can use a running sum  
* ***pushing H*** &rarr; making the deifnition of the derivative more accurate &rarr; the smaller, the closer to the solution  
* when comparing numbers in any numerical computing method, don't expect the exact same numbers &rarr; ***finite precision number*** &rarr; no infinite resolution  

* 2 numbers are considered to be the same up to a certain tolerance/deviation  
```python  
from numpy import isclose
```  

* there are libraries that can calculate the gradient for you  
```python  
from torch import {
    tensor, 
    sum as torch_sum, 
    rand, 
    no_grad
}
from torch.random import manual_seed
```  

### ${\color{red}Check}$  
* operators

### ${\color{red}Questions}$  

### $${\color{blue}Q\&A \space lecture}$$  
