# Calculating square of numbers with unit digit 3

### Parameters

N : Number(integer) whose square is to be calculated

u : unit digit of number(N)

t : number formed after excluding the unit digit

### Formula

```
 R = (N + 5) * t + 2
```

```
Square(N) = Concat(R, 5)
```

### Base of the derivation

```python
>>> for i in range(5, 96, 10):
...     print "%d^2 = %d"%(i, i**2)
... 
5^2 = 25
15^2 = 225
25^2 = 625
35^2 = 1225
45^2 = 2025
55^2 = 3025
65^2 = 4225
75^2 = 5625
85^2 = 7225
95^2 = 9025
>>> 
>>> # Let us omit(unit digit) 5 and calculate the remaining part of 
... # above squares
... 
>>> (5 + 5) * 0 + 2
2
>>> (15 + 5) * 1 + 2     # (N + u) * t + 2  => (N + 5) * t + 2, u will be always 5
22
>>> (25 + 5) * 2 + 2
62
>>> (35 + 5) * 3 + 2
122
>>> (45 + 5) * 4 + 2
202
>>> (55 + 5) * 5 + 2
302
>>> (65 + 5) * 6 + 2
422
>>> 
```

### Example

Calcualte square(685)?

```
Here,
      N = 685
      t = 68

      using formula, (N + 5) * t + 2

      R = (685 + 5) * 68 + 2

      R = 46922

     R5 = 469225	(R and 5 got concatenated)

     square(685) = R5 = 469225
```