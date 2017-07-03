# Calculating square of numbers with unit digit 4

### Parameters

N : Number whose square is to be calculated

u : unit digit of number(N)

t : number formed after excluding the unit digit

### Formula

```
R = (N * (t + 1)) - (3 + t * 6)

R = (N * t) + N - 3 - (t * 6)

R = t * (N - 6) + (N - 3)

R = t * (N - 6) + (N - 6) + 3

R = (N - 6) * (t + 1) + 3
```

```
Square(N) = Concat(R, 6)
```

# Base of the derivation

```python
>>> for number in range(4, 95, 10):
...     print number, "^2 = ", number**2
... 
4 ^2 =  16
14 ^2 =  196
24 ^2 =  576
34 ^2 =  1156
44 ^2 =  1936
54 ^2 =  2916
64 ^2 =  4096
74 ^2 =  5476
84 ^2 =  7056
94 ^2 =  8836
>>> 
>>> 4 * 1 - 3
1
>>> 14 * 2 - 9
19
>>> 24 * 3 - 15
57
>>> 34 * 4 - 21
115
>>> 
```

Or (Using formula **(N - 6) * (t + 1) + 3)**)

```python
>>> for number in range(4, 95, 10):
...     print number, "^2 = ", number**2
... 
4 ^2 =  16
14 ^2 =  196
24 ^2 =  576
34 ^2 =  1156
44 ^2 =  1936
54 ^2 =  2916
64 ^2 =  4096
74 ^2 =  5476
84 ^2 =  7056
94 ^2 =  8836
>>> 
>>> (4 - 6) * (0 + 1) + 3
1
>>> (14 - 6) * (1 + 1) + 3
19
>>> (24 - 6) * (2 + 1) + 3
57
>>> (34 - 6) * (3 + 1) + 3
115
>>> (44 - 6) * (4 + 1) + 3
193
>>> (54 - 6) * (5 + 1) + 3
291
>>> (64 - 6) * (6 + 1) + 3
409
>>> (74 - 6) * (7 + 1) + 3
547
>>> (84 - 6) * (8 + 1) + 3
705
>>> (94 - 6) * (9 + 1) + 3
883
>>> (104 - 6) * (10 + 1) + 3
1081
>>> (994 - 6) * (99 + 1) + 3
98803
>>> 
>>> # Test
... 
>>> 994**2
988036
>>> 34**2
1156
>>> 
```


# Example

Caculate the square of 229?

```
     164 x 164
   =============
       656
      984x
     164xx
   =============
     26896
```

Let's calculate the square of 229 using formula, (N - 6) * (t + 1) + 3

```
Here 
      N = 164
      t = 16
So,
      R = (N - 6) * (t + 1) + 3     
      R = (N - 6) * (t + 1) + 3
      R = (164 - 6) * (16 + 1) + 3
      R = 158 * 17 + 3

Finally

        158 x 17
       ============
          1106
          158x
       ============
          2686

          R = 2686 + 3
          R = 2689
Square(164) = Concat(R, 6)
Square(164) = Concat(2689, 6)
Square(164) = 26896
```