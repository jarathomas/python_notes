# Quick Reference Guide for things I like to do in Python

Useful Python Functions & Examples


## Numpy Random Sampling ([numpy reference](https://numpy.org/doc/stable/reference/random/legacy.html#simple-random-data))

* numbers in [0, 1) (i.e., 1 is *excluded*)
  ```python 
  numpy.random.random(size=(5, 5))
  ```
* integers in [low, high): 
  ```python
  numpy.random.randint(low=0, high=100, size=(5, 5))
  ```
* from a list or numpy.ndarray:
  ```python
  numpy.random.choice(a=["a", "b"], size=(5,5), replace=True, p=[.1, .9])
  ```
  
## Numpy data wrangling

* Table of numpy.ndarray
  ```python
  np.unique(an_array, return_counts=True)
  ```
