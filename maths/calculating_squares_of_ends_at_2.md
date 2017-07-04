# Calculating square of numbers with unit digit 2

### Parameters

N : Number whose square is to be calculated

u : unit digit of number(N)

t : number formed after excluding the unit digit

### Formula

```
R = (N * (t + 1)) - (2 + 8 * t)
R = (N * (t + 1)) - (2 + 8 * t + 8 - 8)
R = (N * (t + 1)) - (6 + 8 * (t + 1))
R = (N - 8) * (t + 1) + 6
```

```
Square(N) = Concat(R ,4)
```

# Base of the derivation

```python
>>> for i in range(2, 93, 10):
...     print i, "^2 = ", i**2
... 
2 ^2 =  4
12 ^2 =  144
22 ^2 =  484
32 ^2 =  1024
42 ^2 =  1764
52 ^2 =  2704
62 ^2 =  3844
72 ^2 =  5184
82 ^2 =  6724
92 ^2 =  8464
>>> 
>>> 2*1 - 2
0
>>> 12*2 - 10
14
>>> 22*3 - 18
48
>>> 32*4 - 26
102
>>> 42*5 - 34
176
>>> 
```

Or 

```python
>>> for i in range(2, 93, 10):
...     print i, "^2 = ", i**2
... 
2 ^2 =  4
12 ^2 =  144
22 ^2 =  484
32 ^2 =  1024
42 ^2 =  1764
52 ^2 =  2704
62 ^2 =  3844
72 ^2 =  5184
82 ^2 =  6724
92 ^2 =  8464
>>> 
>>> 2 * (0 + 1) - 2
0
>>> 12 * (1 + 1) - 10
14
>>> 22 * (2 + 1) - 18
48
>>> 32 * (3 + 1) - 26
102
>>> 42 * (4 + 1) - 34
176
>>> 
```

Or based on (**(N - 8) * (t + 1) + 6**)

```python
>>> for i in range(2, 93, 10):
...     print i, "^2 = ", i**2
... 
2 ^2 =  4
12 ^2 =  144
22 ^2 =  484
32 ^2 =  1024
42 ^2 =  1764
52 ^2 =  2704
62 ^2 =  3844
72 ^2 =  5184
82 ^2 =  6724
92 ^2 =  8464
>>> 
>>> (2 - 8) * (0 + 1) + 6
0
>>> (12 - 8) * (1 + 1) + 6
14
>>> (22 - 8) * (2 + 1) + 6
48
>>> (32 - 8) * (3 + 1) + 6
102
>>> (42 - 8) * (4 + 1) + 6
176
>>>
```
# Example

Caculate the square of 752?

```
     752 x 752
   =============
       1504
      3760x
     5264xx
   =============
     565504
```

Let's calculate the square of 973 using formula, (N - 8) * (t + 1) + 6

```
Here 
      N = 752
      t = 75
So,
      R = (N - 8) * (t + 1) + 6    
      R = (752 - 8) * (75 + 1) + 6
      R = 744 * 76 + 6

Finally

        744 * 76
       ============
         4464
        5208x
       ============
        56544


          R = 56544 + 6
          R = 56550
Square(752) = Concat(R, 4)
Square(752) = Concat(56550, 4)
Square(752) = 565504
```