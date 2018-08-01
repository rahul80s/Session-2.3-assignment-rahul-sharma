# Session-2.3-assignment-rahul-sharma
Acagild session 2.3 assignment 

1. Create an m x n matrix with replicate(m, rnorm(n)) with m=10 column vectors of n=10 elements each,
constructed with rnorm(n), which creates random normal numbers.
Then we transform it into a dataframe (thus 10 observations of 10 variables) and perform an algebraic
operation on each element using a nested for loop: at each iteration, every element referred by the two
indexes is incremented by a sinusoidal function, compare the vectorized and non-vectorized form of creating
the solution and report the system time differences.

Ans 1 ->

set.seed(42);

m=10; n=10;

mymat <- replicate(m, rnorm(n)) 

mydframe=data.frame(mymat)

system.time (mydframe <- mydframe + 10*sin(0.75*pi))

mydframe

