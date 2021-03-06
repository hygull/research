# Calculating square of numbers with unit digit 8

### Parameters

N : Number whose square is to be calculated

u : unit digit of number(N)

t : number formed after excluding the unit digit

### Formula

```
R = (N * (t + 1))  - (2 * (t + 1))

R = (N - 2) * (t + 1)
```

```
Square(N) = Concat(R, 4)
```

# Base of the derivation

```python	
>>> for i in range(8, 99, 10):
...     print i, "^2 = ", i**2
... 
8 ^2 =  64
18 ^2 =  324
28 ^2 =  784
38 ^2 =  1444
48 ^2 =  2304
58 ^2 =  3364
68 ^2 =  4624
78 ^2 =  6084
88 ^2 =  7744
98 ^2 =  9604
>>> 
>>> (8 * (0 + 1)) - (2 * ( 0 + 1))
6
>>> (18 * (1 + 1)) - (2 * ( 1 + 1))
32
>>> (28 * (2 + 1)) - (2 * ( 2 + 1))
78
>>> (38 * (3 + 1)) - (2 * ( 3 + 1))
144
>>> (48 * (4 + 1)) - (2 * ( 4 + 1))
230
>>> (58 * (5 + 1)) - (2 * ( 5 + 1))
336
>>> (68 * (6 + 1)) - (2 * ( 6 + 1))
462
>>> (78 * (7+ 1)) - (2 * ( 7 + 1))
608
>>> (88 * (8 + 1)) - (2 * ( 8 + 1))
774
>>> (98 * (9 + 1)) - (2 * ( 9 + 1))
960
>>> (108 * (10 + 1)) - (2 * ( 10 + 1))
1166
>>> 
```

Or (Based on the formula **R = (N - 2) * (t + 1)**)

```python
>>> for i in range(8, 99, 10):
...     print i, "^2 = ", i**2
... 
8 ^2 =  64
18 ^2 =  324
28 ^2 =  784
38 ^2 =  1444
48 ^2 =  2304
58 ^2 =  3364
68 ^2 =  4624
78 ^2 =  6084
88 ^2 =  7744
98 ^2 =  9604
>>> 
>>> (8 - 2) * (0 + 1)
6
>>> (18 - 2) * (1 + 1)
32
>>> (28 - 2) * (2 + 1)
78
>>> (38 - 2) * (3 + 1)
144
>>> (48 - 2) * (4 + 1)
230
>>> (58 - 2) * (5 + 1)
336
>>> (68 - 2) * (6 + 1)
462
>>> (78 - 2) * (7 + 1)
608
>>> (88 - 2) * (8 + 1)
774
>>> (98 - 2) * (9 + 1)
960
>>> (108 - 2) * (10 + 1)
1166
>>> 
```

# Example

Caculate the square of 338?

```
     348 x 348
   =============
       2784
      1392x
     1044xx
   =============
     121104
```

Let's calculate the square of 229 using formula, (N - 1) * (t + 1)

```
Here 
      N = 348
      t = 34
So,
      R = (N - 2) * (t + 1)     
      R = (348 - 2) * (34 + 1)
      R = 346 * 35

Finally

        346 * 35
       ============
         1730 
        1038x
       ============
        12110


          R = 12110
Square(348) = Concat(R, 4)
Square(348) = Concat(12110, 4)
Square(348) = 121104
```