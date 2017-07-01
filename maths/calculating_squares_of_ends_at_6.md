# Calculating squares of numbers with unit digit 6

### Parameters

N : Number whose square is to be calculated

u : unit digit of number(N)

t : number formed after excluding the unit digit

### Formula

```
R = (N-4)*(t + 1) + 1
```

```
Square(N) = Concat(R, 6)
```

### Base of the derivation

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
>>> 6  * (0+1) - 3     # 06 * (0+1) - 3
3
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
>>> 226 * (22 + 1) - (3 + 4*(22))   # A.P, a=7, d=4, then 22th term will be 7 + 4*(22-1)
5107
>>> 
```

The last terms of each of the above evaluations are in A.P

where first term is **a=3**, common difference is **d=4**

Then nth term **Term_n** can be calculated as follows

```
  Term_n = a+(n-1)*d

  Term_1 = 3+(1-1)*4 = 3

  Term_2 = 3+(2-1)*4 = 7
```

And the nth **number formed after ignoring the unit digit** will be 1 less than the term number(n-1).

**eg.**

16, the 2nd term, will give 1 (when we ignore the unit digit) which is 1 less than the term number

56, the 6th term, will give 5 (when we ignore the unit digit) which is 1 less than the term number

So in expression **3+(n-1)\*4**, (n-1) denotes the **number formed after ignoring the unit digit**.

And we will represent **(n-1)** as **t**. 

So **Term_n** = **3+(n-1)\*4** = **3+t*4** 

226 will be 23rd term in A.P. 6, 16, 26, 36, ...

```
226 * (22 + 1) - (3 + 4*(23-1))  
      ||
      \/
226 * (22 + 1) - (3 + 4*(22))  
```

```
tu * (t+1) - (3 + 4 * (t))

tu * (t + 1) -3 - 4t

tu * (t + 1) - 3 - 4t

tu * t + tu - 3 - 4t

(tu - 4) * t + tu - 4 + 1

(tu - 4) * (t + 1) + 1

(N - 4) * (t + 1) + 1
```

### Example

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

Let's use formula,(N=96 ,t=9, u=6)

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

### More examples

Calculate square(56)?

```
  Here N = 56, t = 5

  So,
     56^2 =  (56-4) * (5+1) + 1
          =  52*6 + 1
          =  312 + 1
      R   =  313
      R6  =  3136   (Concatenation of R and 6)
```


Calculate square(234576)?

```
  Here N = 234576, t = 23457

  So,
     234576^2 =  (234576-4) * (23457+1) + 1
              =  234572*23458 + 1
              =  5502589976 + 1
         R    =  5502589977
         R6   =  55025899776    (Concatenation of R and 6)
```


