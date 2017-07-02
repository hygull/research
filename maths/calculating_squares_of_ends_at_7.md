# Calculating square of numbers with unit digit 7

### Parameters

N : Number whose square is to be calculated

u : unit digit of number(N)

t : number formed after excluding the unit digit

### Formula

```
R = (N * (t + 1)) - (3 * (t + 1))

R = (N - 3) * (t + 1)
```

```
Square(N) = Concat(R, 9)
```

# Base of the derivation

```python
>>> for number in range(7, 98, 10):
...     print number, "^2 = ", number**2
... 
7 ^2 =  49
17 ^2 =  289
27 ^2 =  729
37 ^2 =  1369
47 ^2 =  2209
57 ^2 =  3249
67 ^2 =  4489
77 ^2 =  5929
87 ^2 =  7569
97 ^2 =  9409
>>> 
>>> 7 * 1 - 3
4
>>> 7 * (0 + 1) - 3
4
>>> 17 * (1 + 1) - 6
28
>>> 27 * (2 + 1) - 9
72
>>> 37 * (3 + 1) - 12
136
>>> 47 * (4 + 1) - 15
220
>>> 57 * (5 + 1) - 18
324
>>> 67 * (6 + 1) - 21
448
>>> 77 * (7 + 1) - 24
592
>>> 87 * (8 + 1) - 27
756
>>> 97 * (9 + 1) - 30
940
>>> 
```

Or

```python
>>> for number in range(7, 98, 10):
...     print number, "^2 = ", number**2
... 
7 ^2 =  49
17 ^2 =  289
27 ^2 =  729
37 ^2 =  1369
47 ^2 =  2209
57 ^2 =  3249
67 ^2 =  4489
77 ^2 =  5929
87 ^2 =  7569
97 ^2 =  9409
>>> 
>>> 7 * (0 + 1) - (3 * (0 + 1))
4
>>> 17 * (1 + 1) - (3 * (1 + 1))
28
>>> 27 * (2 + 1) - (3 * (2 + 1))
72
>>> 
```

Or (Based on the formula **R = (N - 3) * (t + 1)**)

```python
>>> for number in range(7, 58, 10):
...     print number, "^2 = ", number**2
... 
7 ^2 =  49
17 ^2 =  289
27 ^2 =  729
37 ^2 =  1369
47 ^2 =  2209
57 ^2 =  3249
>>> 
>>> (7 - 3) * (0 + 1)
4
>>> (17 - 3) * (1 + 1)
28
>>> (27 - 3) * (2 + 1)
72
>>> (37 - 3) * (3 + 1)
136
>>> (47 - 3) * (4 + 1)
220
>>> (57 - 3) * (5 + 1)
324
>>> 
```



# Example

Caculate the square of 147?

```
     147 x 147
   =============
       1029
       588x
      147xx
   =============
      21609
```

Let's calculate the square of 229 using formula, (N - 3) * (t + 1)

```
Here 
      N = 147
      t = 14
So,
      R = (N - 3) * (t + 1)     
      R = (147 - 3) * (14 + 1)
      R = 144 * 15

Finally

        144 * 15
       ============
          720 
         144x
       ============
         2160


          R = 2160
Square(147) = Concat(R, 9)
Square(147) = Concat(2160, 9)
Square(147) = 21609
```