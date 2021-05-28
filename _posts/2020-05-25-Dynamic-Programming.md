---
layout: post
title:  "Dynamic Programming"
date:   2021-05-25 16:41:58 -0500
categories: jekyll update
readtime: true
tags: [DP]
---
**Idea:** The idea of dynamic programming(DP) is breaking down a **large, complex** problem into **smaller, simple** problems. 

Example: 

1. For fibonacci sequences, instead of finding a complex function that returns the nth fibonacci number, we can use DP to break the problem into a simpler problem which is to find the next fibonacci number using the latest fibonacci number.

2. For the problem of finding the number of paths from point x to point y on a grid, instead of finding the final answer, we can use DP to find the number of paths to each cell depending on the next last cell. 

There are two seperate approaches to dynamic programming, bottom-up and top-down. 

**Bottom-up:** Let’s describe a state for our DP problem to be dp[x] with dp[0] as base state and dp[n] as our destination state. So,  we need to find the value of destination state i.e dp[n]. 

This method is also called *"Tabulation"* because we need a tabulated version of the original data stucture.

```java
// Tabulated version to find factorial x.
int dp[MAXN];

// base case
int dp[0] = 1;
for (int i = 1; i< =n; i++)
{
    dp[i] = dp[i-1] * i;
}
```

**Top-down:** If we need to find the value for some state say dp[n] and instead of starting from the base state that i.e dp[0] we ask our answer from the states that can reach the destination state dp[n] following the state transition relation, then it is the top-down fashion of DP. 

This method is also called *"Memorization"* because we need the memorized verion of the last state.

```java
// Memoized version to find factorial x.
// To speed up we store the values
// of calculated states

// initialized to -1
int dp[MAXN]

// return fact x!
int solve(int x)
{
    if (x==0)
        return 1;
    if (dp[x]!=-1)
        return dp[x];
    return (dp[x] = x * solve(x-1));
}
```

**5 Easy Steps to DP:**
1. Visualize Example
2. Find an appropriate subproblem
3. Generalize the relationship
4. Implement by solving subproblems in order




