# Climbing-Stairs
You are climbing a staircase. It takes n steps to reach the top.  Each time you can either climb 1 or 2 steps. In how many distinct ways can you climb to the top?   

class Solution:
    def climbStairs(self, n):
        if n == 1:
            return 1
        if n == 2:
            return 2

        ways = [0] * (n + 1)
        ways[1] = 1
        ways[2] = 2

        for i in range(3, n + 1):
            ways[i] = ways[i - 1] + ways[i - 2]

        return ways[n]

sol = Solution()
print(sol.climbStairs(2)) 
print(sol.climbStairs(3)) 
