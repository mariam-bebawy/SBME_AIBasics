## $${Lecture \space 2}$$  
### ${\color{red}Notes}$  
* seed &rarr; generate the same random points  
* *read open source code to understand papers and more comprehensive codes*  
* output difference depending on how you call random seed functions  
* plotting &rarr; using proper object oriented API of ***matplotlib***  
* ***zip*** function returns generator &rarr; zipping along list length dimension  
* in neural networks, you're not looking for ***(x, y)***, you're looking for parameters  
* gradient descent &rarr; just go in the opposite direction of the derivative ***to minimize***  
* always go back to first principles  
* please write the code to embed it in your mind  

### ${\color{red}Check}$  
* list comprehension  
* $${L = \dfrac{1}{N} \sum_{i=0}^{N-1}[(x_i - x_p)^2 + (y_i - y_p)^2]^\frac{1}{2}}$$  
$${L = argmin(x_p, y_p)}$$
```python  
def loss(x_p, y_p):
    return(1/len(data_x)) * sum(
        [sqrt((x_i - x_p)**2 + (y_i - y_p)**2)
            for x_i, y_i in zip(data_x, data_y)]
    )
```  

### ${\color{red}Questions}$  
* code convention  
* decorators  

### $${\color{blue}Q\&A \space lecture}$$  
#### ***list comprehension***  
* scientific writing &rarr; try sending conference papers  
* low readability  
* rules in functional programming  
```python
lst_x = []
for i in range(10):
    lst_x.append(i)     # O(1) is the wrong answer
    # AMORTIZED is the right answer

lst_x = [ i for i in range(10) ]
```
* `range` returns generator &rarr; returns point by point  
* generator &rarr; `range(10)` &rarr; ***lazy loading***  
* returns reference to the current value  
```python
lst = []
for i in range(10):
    for j in range(10):
        lst.append(i*j)

lst = [ i*j for i in range(10) for j in range(10) ]
```

```python
dict = { K:0 for K in range(10) }
```
```python
class lectures:
    def __iter__(self):
        return self
    def __next__():
        pass
```
*to design iterator:*  
1. get iterable object  
1. define bnext behaviour  
1. start &rarr; next step &rarr; end  

```python
def rng_gen():
    for in range(10):
        yield i
for x in rnd_gen():
    print(x)
```  

#### ***why not design all functions in the same way of the literal loss function ?***
* any *differentiable* arbitrary function  
* neural network &rarr; some parameters + loss function  
* compute loss function and move against the flow  
* *numerically* &rarr; it's the same procedure all the time  
* *efficiently though ?* &rarr; you're computing on all values on all parameters  
* there's no better computation for the gradient &rarr; we can only ***optimize***  
* ***efficiency on scaling*** &rarr; ktr el parameter models w ktr el values  

#### ***decorators***  
* simply bta5od function w btrg3 function  
* momkn tzwd 7aga ablha w momkn tzwd 7aga b3dha  

#### ***how to visualize loss fucntion***  
* `x_p`, `y_p`, and `z` is the loss function  
* to compute loss for 1 candidate data point, i must compute on all points  

#### ***what does it mean to go against the gradient***  
* `stem = 3d`  
* grb tsbt value ll `y_p` w visualize el `x_p`  
* the gradient descent step depends on the value of the derivative  

#### ***deep learning in general***
* tokens in discrete values  
* memorization algorithms  
* emergent properties &rarr; prompting  
* doesn't have reasoning  
* learning theory  
* no free launch  
* data governs learning  
* federated learning &rarr; ***cruise***  
* how the algorithm can evlove its learning  
* generative AI &rarr; *fitting*  
* prompting means more biasing  

## quiz next time &rarr; expect coding parts  
