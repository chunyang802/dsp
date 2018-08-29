[Think Stats Chapter 8 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2009.html#toc77) (scoring)

>> ```python
n=[10,100,1000]

def SimulateSample(n):
    estimates =[]
    for _ in range (1000):
        xs = [np.random.exponential(1.0/2,n)]
        estimate =1/np.mean(xs)
        estimates.append(estimate)
    
    
    stderr = RMSE(estimates,lamda)
    return stderr
#print (SimulateSample(10))

def n_stderr(n):
    stderrs = []
    for number in n:
        print ('number', number)
        stderr = SimulateSample(number)
        print ('stderr', stderr)
        stderrs.append(stderr)
    return stderrs

#print (n_stderr([10,100,1000]))

thinkplot.Scatter(n,n_stderr(n))
```
As the sample number increases, the standard error decreases. 


