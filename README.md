# PyBOBYQA (Bound Otimization by Quadratic Approximation)

Derivative free optimization methods also referred as black box optimization method are easy to use methods as it allows us not to worry about gradients.
BoundOptimization by Quadratic Approximation is one such method where the optimal points of a function is located by quadratic approximation of the function at 
each step. Depending on the number of dimensions some values of the function at some initial points are calculated. For example, for one dimension, quadratic function takes the form ax<sup>2</sup> + bx + c meaning we need to make 3 function evaluation to get tha value of a,b and c. Using these a quadratic approximation of the function is obtained and its minima is found. In the next step one of the earlier calculated points with maximum function value is replaced with the minima and new quadratic approximation is derived. This process is repeated until convergence.

## Installation and Usage

Installation using pip
` $ [sudo] pip install Py-BOBYQA `

If no sudo privileges

`$ pip install --user Py-BOBYQA`

The requirements for this optimization package are straightforward. A function that accepts the parameters to be optimized and returns the value. An example of usage of this function :

```python
import pybobyqa
import numpy as np

def square(x):
    return sum((x - .5)**2)

x0 = np.array([5.0, -20.0])
soln = pybobyqa.solve(freudenstein_roth, x0, maxfun=500, bounds=(lower, upper))
print(soln.x)

>>> [0.5,0.5]
```

## Citations 

Cartis, C., Fiala, J., Marteau, B. and Roberts, L., Improving the Flexibility and Robustness of Model-Based Derivative-Free Optimization Solvers, *ACM Transactions on Mathematical Software*, 45:3 (2019), pp. 32:1-32:41.

Cartis, C., Roberts, L. and Sheridan-Methven, O., Escaping local minima with derivative-free methods: a numerical investigation, technical report, University of Oxford, (2018).

## Assesment
While the method is easy to install and implement, it takes a long time to reach an optimal solution. The method improves upon the baseline but it takes around 8.5 minutes per file rendering it unfit for our use.

key metrics :

- Runtime
- Performance (Loss Metric)
- Complexity of Implementation
- Specialized Hardware/Software/Framework Requirements
