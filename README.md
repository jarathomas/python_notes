# Quick Reference Guide for things I like to do in Python

Useful Python Functions & Examples

## Pandas

* Something similar to R's `match(a, b)` function (i.e., return indicies of b that match each element of a)
  ```python
  # in R: match(c(1, 5, 10, 15), c(5, 1, 10)) gives: 2 1 3 NA
  alist = [5, 10, 15]
  [alist.index(i) if i in alist else np.nan for i in pd.Series([1, 5, 10, 15])]
  # so you may need to turn a DataFrame into a list
  # (still seems like there should be an easier way)
  ```
  
* Tabulations & Crosstabs
  ```python
  # from pandas import crosstab, DataFrame
  df = DataFrame({"age": "child", "race": 1}, {"age": "child", "race": 1},
                 {"age": "child", "race": 1}, {"age": "child", "race": 2},
                 {"age": "adult", "race": 1}, {"age": "adult", "race": 1},
                 {"age": "adult", "race": 2}, {"age": "adult", "race": 3})

  df["age"].sort_values(ascending = False)
  crosstab(df["age"], df["race"])
  # table for one variable
  df.age.value_counts(normalize = False, sort = True, ascending = True, bins = None, dropna = True)
  ```


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
