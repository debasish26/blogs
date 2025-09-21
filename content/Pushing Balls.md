
[**Pushing Balls**](https://codeforces.com/contest/2090/problem/B) : This is an implementation Heavy Problem I considered it as a interestingly bad and weird problem (don't like grid problems that much).
	
**Key idea** of this problem is that to just check if any grid is set is that position is valid for it or not. That's it 

**Observation :** For this problem a grid can be 1 if the grid(i-1 ,j)or grid(i,j-1) is 0 then possibility is false lets say these are leftzeros and rightzeros but if only 1 row or at i == 0 then this can give **Run Time Error** so extra conditions for them as i should be > 0 and j should be > 0

You can find the complete implementation Here. **[Pushing Balls.](https://codeforces.com/contest/2090/submission/339282702)**