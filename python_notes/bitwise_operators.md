# Bitwise Operators

# Converting between Binary and Integer

## Binary -> Integer

```python
int( bin_num, base=2)

>>> int('0b101', base=2)
5

>>> int('101', base=2)
5
```

## Integer to Binary
```python
bin(int_num)

>>> bin(3)
'0b11'

```

# Operators

## Complement
```python
~ x
```
Returns the complement of x - the number you get by switching each 1 for a 0 and each 0 for a 1. This is the same as -x - 1.

### Example
```
N = 5 = (101)2 
~N = ~5 = ~(101)2 = (010)2 = 2
```

## Bit-Shift Left
```python
x << y
```
Returns x with the bits shifted to the left by y places (and new bits on the right-hand-side are zeros). 
This is the same as multiplying x by 2**y.

## Bit-Shift Right
```python
x >> y
```
Returns x with the bits shifted to the right by y places. This is the same as //'ing x by 2**y.

## Bit-wise AND
```python
x & y
```
Does a "bitwise and". Each bit of the output is 1 if the corresponding bit of x AND of y is 1, otherwise it's 0.


## Bit-wise OR
```python
x | y
```
Does a "bitwise or". Each bit of the output is 0 if the corresponding bit of x AND of y is 0, otherwise it's 1.


## Bitwise Exclusive OR (XOR)
```python
x ^ y
```
Does a "bitwise exclusive or". Each bit of the output is the same as the corresponding bit in x if that bit in y is 0, and it's the complement of the bit in x if that bit in y is 1.
