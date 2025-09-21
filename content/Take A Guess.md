
[**Take A Guess**](https://codeforces.com/contest/1556/problem/D) : This is an interactive problem that means need to take response from the online judge.
	
**Key idea** of this problem is that it works on some Mathematical Ideas with
Some Bitwise Properties. Let's look into the ideas and formulas:
we can find 3 different numbers from addition  :

```
a + b = p
a + c = q
b + c = r
```
									
Now we can find a from here as :
```
a = (p + q - r)/2
```

after getting a we can easily get b and c 

Now we don't know a and b yet so how do we find a + b (using & and | given by the judge)
We will use some bitwise properties here:
```
a + b = 2*(a&b)+a^b 
```

as a ^ b will give all possible set values for a and b excludes common set bits to tackle this we will add these bits again by doing a&b which will give all the common set bits as after adding bite move left 1 bits like 1 + 1 = 10 (in binary) we multiply 2. But we don't know a ^ b yet we can get it from a & b and a|b which we know, By:

```
a ^ b = (a|b) - (a&b)
```

Logic is from all bits which are set remove the bits which are common to get a ^ b

**Observation :** for this is if i somehow know the first 3 integers of the array i can find 4th one then 5th one and then nth one and then sort the array and can return the kth element.

Now how to get the first 3 elements by using all the key ideas i mentioned.

And That's our solution.

You can find the complete implementation Here. **[Take A Guess.](https://codeforces.com/contest/1556/submission/338134863)**