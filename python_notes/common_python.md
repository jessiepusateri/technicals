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
### reversed()

### slicing

```python
a[start:end] # items start through end-1
a[start:]    # items start through the rest of the array
a[:end]      # items from the beginning through end-1
a[:]         # a copy of the whole array
```
```python
> a = [1, 2, 3, 4, 5]
> b = a[:2]
> b
=> [1, 2]
> c = a[3:]
> c
=> [4, 5]
```

### zip(*iterables)
Make an iterator that aggregates elements from each of the iterables.

Returns an iterator of tuples, where the i-th tuple contains the i-th element from each of the argument sequences or iterables. The iterator stops when the shortest input iterable is exhausted. 

```python
>>> x = [1, 2, 3]
>>> y = [4, 5, 6]
>>> zipped = zip(x, y)
>>> list(zipped)
[(1, 4), (2, 5), (3, 6)]
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

### Strings and Tuples are Immutable

Tuples
```python
>>> int_tuple = (4, 9)
>>> int_tuple[0] = 1
# raises: TypeError: 'tuple' object does not support item assignment
```

Strings
```python
>>> test_string = 'mutable?'
>>> test_string[7] = '!'
# TypeError: 'str' object does not support item assignment
```

### enumerate and reverse


### Template

  ```python
  >
  =>
  ```
