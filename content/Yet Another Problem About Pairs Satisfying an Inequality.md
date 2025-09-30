[**Yet Another Problem About Pairs Satisfying an Inequality**](https://codeforces.com/problemset/problem/1703/F) : At first it seems to me as an easy question i just need to findout the pair and as n = 1e5 i can easily run a nlog n complexity code like this

```
for(int i =0;i<n;i++){
	for(int j = i + 1;j<n;j++){
		// logic here
	}
}
```

At First it seems for i = 0 it will run n-1 loop and for i = n-2 it will run only 1 loop so complexity should be in the bound ?? But no for some reason this code give me TLE a test case 4 so i understand i am calculating T.C wrong

Lets see the optimal approach here :

**Key Idea** of this problem is to find pairs right so lets see the equation first
```
a[i] < i < a[j] < j
```

which says need to find such pairs where index will be greater then its value note that it's a 1 based index system

after finding such index we need to check if they can make pair or not.

Now to check that we can use **lowerbound** of binary search

**Observation** is that if we filter out the value which satisfies as ai < i then among them we need to determine is any index in my filtered array (this array will contain only indices) which is less than ai if yes how many these can make pairs.

You can find the complete implementation Here. **[Yet Another Problem About Pairs Satisfying an Inequality.](https://codeforces.com/contest/1703/submission/341145432)**


