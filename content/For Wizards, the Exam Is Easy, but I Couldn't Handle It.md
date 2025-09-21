
[**For Wizards, the Exam Is Easy, but I Couldn't Handle It**](https://codeforces.com/contest/2072/problem/D) : Not your usual greedy and implementation question need some logical observation and optimisation.
	
**Key idea**: The key idea of this question is calculate which l and r can make the inversion count less. So to do that we can count which l and r after switching can reduce the count.
First i thought that is related to somehow inversion count using merge sort but no its a simple but logical thinking things.

**Observation :** I found first observation as if i choose 2 indices the inversion between them will not be affected only the inversion related to l will change so need to found that one l and r. Now how ?

Then i notice the n is 1e6 can run a loop where so why not for every l from 0 to n-1 count if a(r) < a(l) means l has that elements inversion so what if instead of couting inversion i will count after ops how many inversion will fix so if a(r) < a(l) means after ops it will be fix so cnt++ but at same time need to count if its making any inversion so if any a(r) > (l) then cnt--
now if cnt goes maximum than ans then update it and l and r also and thats my ans

Now Time complexity

0 1 2 3 4 5
for 0 loop will go till 5
for 1 -> 1 to 5
for 2 -> 2 to 5
for 3 -> 3 to 5
for 4 -> 4 to 5
now for 5 -> 5 to 5

so it will be bellow n^2 so **yes this will work Boom.**

You can find the complete implementation Here. **[For Wizards, the Exam Is Easy, but I Couldn't Handle It](https://codeforces.com/contest/2072/submission/339508335)**
