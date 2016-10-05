# Jack-Car-Rental-using-Policy-Iteration
This program is to find optimal policy over Jack's cars rental problem using policy iteration. There <br />
are 2 locations (e.g. A and B) with initially 20 cars in each side. Cars in both location are rented <br />
and returned according to certain distribution. Every night, we can move 5 cars from A to B or from <br />
B to A. Cars moved in overnight plus remaining cars (not rented) cannot surpass 20. The maximum <br />
number of cars to be rented in the next day is cars moved in overnight plus remaining cars on this <br />
day. The  number  of  cars  requested  and  returned  at each location are Poisson random variables <br />
with λ as expected value. Assume λ is 3 and 4 for rental requests at locations A and B, and 3 and 2 <br />
for returns. We can earn $10 for one car rental and cost $2 for moving one car overnight. <br />T
The original description about Jack's cars rental problem can be found in [here](https://webdocs.cs.ualberta.ca/~sutton/book/the-book.html).

# Implementation
Still working on

# Result
The following shows errors of value function in policy evaluation, the improved policy in that iteration <br />
(the one shown in the figure is the optimal policy), and the error between improved policy and original <br />
policy (error = 0 means we get the optimal policy). <br />
![alt tag](https://github.com/TsunHsuang-Wang/Jack-Car-Rental-using-Policy-Iteration/blob/master/img/result.png) <br />
row[0:20] --> number of cars in location A is 0~20 <br />
col[0:20] --> number of cars in location B is 0~20 <br />

# Requirement
numpy<br />
scipy<br />
argparse<br />

# How to run
If using the precomputed matrices associated with environmental dynamics, just type in your terminal <br />
```
$ python main.py
```
If you want to formulate a different problem setting (e.g. with different number of cars or number <br /> 
of moves), you can type <br />
```
$ python main.py --to_form_all True --params your_params
```
It will form and save .npy file in the same directory, and next time with the same problem setting, <br />
you can simply load that .npy file, which may save a lot of time.
You can get basic documentation from typing <br />
```
$ python main.py --help
```
There are several parameters able to be adjusted. <br />
Also, you can modify default value in file parameters.py <br />

# Author
Tsun-Hsuang, Johnson, Wang
