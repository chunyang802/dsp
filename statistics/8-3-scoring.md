[Think Stats Chapter 8 Exercise 3](http://greenteapress.com/thinkstats2/html/thinkstats2009.html#toc77)

---

>> 
```python
def SimulateGames(lam):
    t = 0
    goal = 0 
    while True:
        time_interval = random.expovariate(lam)
        t+=time_interval
        if t>1:
            break
        goal+=1
        
    L=goal
    return goal

def Estimate6(m =10000):
    estimates = []
    for i in range (m):
        estimate = SimulateGames(2)
        estimates.append(estimate)
    pmf = thinkstats2.Pmf(estimates)
    thinkplot.Hist(pmf)
        
Estimate6()
```
