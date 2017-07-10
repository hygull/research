# Theorem

For every odd number(**odd**) there exists a perfect square number(**p1**) so that sum of perfect square(p1) & odd number(odd) would generate another perfect square number(**p2**).

### Parameters

```
p1  : perfect square number

odd : odd number

p2  : perfect square number
```

And

```
p2 = p1 + odd
```

where

```
p1 = ((odd - 1) ^ 2) / 4
```

### Derivation of ((odd - 1) ^ 2) / 4

```
As we know,

	0 + 1 = 1
	1 + 3 = 4
	4 + 5 = 9
	9 + 7 = 16
	16 + 9 = 25
	25 + 11 = 36
	36 + 13 = 49
	49 + 15 = 64
	64 + 17 = 81

```

**n**th term of the arithmetic progression 1, 3, 5, 7, 9, ... is **1 + (n - 1) \* 2**

Once we got the term number(n) of any odd number then we can easily find its corresponding perfect square number (**p1**) by calculating **(n-1) ^ 2**.

Now let us covert the above expression  **(n-1) ^ 2** in terms of odd number(**odd**).

Let **n**th term of progression 1, 3, 5, 7, 9, ... is **n**

then,

```
odd = 1 + (n - 1) * 2
```

where

```
	odd : nth odd number
	a   : 1 (first term)	 
	d   : 2 (common difference)
```

so

```
	odd = a + (n - 1) * d

	odd = 1 + (n - 1) * 2
```

**odd** is known, so we have to find the value of **n** and **(n-1) ^ 2** will give the value of **p1**

so

```
	n - 1 = ((odd - 1) / 2) 

	p1 = (n - 1) ^ 2  = ((odd - 1) / 2) ^ 2
```

### Examples

##### Find the perfect square corresponding to **1**.

```
	odd = 1
	p1  = ((1 - 1) ^ 2) /4
	p1  = 0 / 4
	p1  = 0

then 
	p2 = p1 + odd
	p2 = 0  + 1
	p2 = 1
``` 

##### Find the perfect square corresponding to **9**.

```
	odd = 9
	p1  = ((9 - 1) ^ 2) /4
	p1  = 64 / 4
	p1  = 16
	
then 
	p2 = p1 + odd
	p2 = 16 + 9
	p2 = 25
``` 

