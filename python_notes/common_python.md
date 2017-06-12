# Cool Python Things

## Built-In Functions

### filter(function, iterable)
  Construct a list from these elemts of iterable for which function returns true.

  ```python
  > filter(lambda x: x == 1, [1, 2, 3])
  => [1]
  ```

### map(function, iterable)
  Apply funtion to every item of iterable and return a list of the results.

  ```python
  > celsius = [39.2, 36.5, 37.3, 37.8]
  > map( lambda x: (float(9/5) * x + 32), celsius)
  => [102.56, 97.7, 99.14]
  ```

### reduce(function, iterable)
  Apply function of two arguments cumulatively to the items of iterable, from left to right, so as to reduce the iterable to a single value.

  ```python
  > reduce(lambda x, y: x + y, [1, 2, 3, 4, 5])
  => 15
  ```

### string.join(words [, sep])
  Concatenate a list or tuple of words with intervening occurences of sep.

  ```python
  >"".join(['h', 'i']
  => "hi"
  ```
  
### enumerate(iterator/sequence)
  Returns an iterator of thing...(0, thing[0]), (1, thing[1]), (2, thing[2])

### xrange(start, stop)
  This function is very similar to range() but returns an xrange object instead of a list.

  ```python
  >
  =>
  ```

## Tricks

### Trick: Assigning whichever variable is not null.
  When one of the variables is null and you want to assign the one that is not null, you can use "or".
  ```python
  > a = 1
  > b = None
  > c = a or b
  > c
  => 1
  ```

## Behavior

### Division is Floor Division

```python
>8/7
>>>1

```
floor(8.0/7.0) == floor(1.14) == 1

```python
>8/-7
>>>-2
```
floor(8.0/7.0) == floor(-1.14) == -2


### Template

  ```python
  >
  =>
  ```
