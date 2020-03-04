```python
import pandas as pd
import numpy as np
import matplotlib.pyplot  as plt
%matplotlib inline
import seaborn as sns
import math as m
import sympy as sp
from sympy import *
import sympy as spy
from sympy import Array
pd.set_option('display.max_columns', 100)

pd.set_option('display.max_rows', 100)

pd.set_option('display.width', 100)

```


```python
y1, y2, y3, z1, z2, z3, x, y, z = symbols('y1, y2, y3, z1, z2, z3 x z y')
```


```python
# program that takes sum and product

def product_sum (num1, num2, num3):
    diff = num2 - num1
    product = num3 * diff
    print(product)


def main ():
    product_sum (4, 10, 6)
    num1 = int(input('enter any integer: '))
    num2 = int(input('enter any integer: '))
    num3 = int(input('enter any integer: '))
    product_sum (num1, num2, num3)
    
    
main ()
```

    36
    

    enter any integer:  3
    enter any integer:  6
    enter any integer:  3
    

    9
    


```python
# the product of a certain number and 5 is two twice the number and substract from 20

def word_problem(x, y, z, c):

    eqn = spy.Eq (z - c * x,  y * x)
    ans = spy.solve((eqn), (x))
    
    print('The number is: {0}'.format(ans[0]))
    
    def confirmatory_test(value):
        subl =Array([y * x]).subs(x, value)
        print('Left hand side: {0}'.format(subl[0]))
        subR =Array([z - c * x]).subs(x, value)
        print('Right hand side: {0}'.format(subR[0]))
        if subl == subR:
            print('The solution is correct\n' + 
                  'since lelt hand side is equal to the Right hand side of the equation')
        else:
            print('wrong! Please check your wouking')
            
    confirmatory_test(ans[0])
    
    
def main ():
    word_problem(x, 5, 20, 2)
    
    
main()
```

    The number is: 20/7
    Left hand side: 100/7
    Right hand side: 100/7
    The solution is correct
    since lelt hand side is equal to the Right hand side of the equation
    


```python
v = 5
subl =Array([z - 2 * x]).subs(x, v)
print(subl)
```

    [y - 10]
    


```python

```
