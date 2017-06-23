# Mathematics

### Calculating squares of numbers ending with digit 6

##### Derivation

```python
>>> for i in range(16, 97, 10):
...     print "%d^2 = %d" % (i, i**2)
... 
16^2 = 256
26^2 = 676
36^2 = 1296
46^2 = 2116
56^2 = 3136
66^2 = 4356
76^2 = 5776
86^2 = 7396
96^2 = 9216
>>> 
>>> 16 * (1+1) - 7
25
>>> 26 * (2+1) - 11
67
>>> 36 * (3+1) - 15
129
>>> 46 * (4+1) - 19
211
>>> 56 * (5+1) - 23
313
>>> 66 * (6+1) - 27
435
>>> 76 * (7+1) - 31
577
>>> 86 * (8+1) - 35
739
>>> 96 * (9+1) - 39
921
>>> 226 * (22 + 1) - (7 + 4*(22-1))   # A.P, a=7, d=4, then 22th term will be 7 + 4*(22-1
5107
>>> 
```

```
226 + (22 + 1) - ( 7 + 4 * (22 - 1) )

tu * (t+1) - (7 + 4 * (t - 1))

tu * (t + 1) -(7 + 4t - 4)

tu * (t + 1) - 3 - 4t

tu * t + tu - 3 - 4t

(tu - 4) * t + tu - 4 +1

(tu - 4) * (t + 1) + 1
```

### Examples

```
If N = tu = 16 (t is concatenated with u)

then t=1, u=6	

Using 
        R  = (N-4)*(t + 1) + 1
 
        R  = (16-4) * (1 + 1) + 1 = 25

        R6 = 256	(R and 6 are concatenated)
```

### Advantages

Here we will multiply 96 with 96.

```
    96x96
   =======
      576
   + 864x
   -------
     9216
```

Let's use formula,(t=9, u=6)

```
    R = (N-4)*(t + 1) + 1

    R = 92*10 + 1

    R = 921

    R6 = 9216
```

We only multiplied 92 with 10(Not 96 with 96).
```
    92x10
   =======
      000
   +  92x
   -------
      920
```
