[Think Stats Chapter 7 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2008.html#toc70) (weight vs. age)

>> 
```python
import first

live, firsts, others = first.MakeFrames()
live = live.dropna(subset=['agepreg', 'totalwgt_lb'])
age = live.agepreg
weights = live.totalwgt_lb
thinkplot.Scatter(age, weights, alpha = 1.0)
thinkplot.Config(xlabel = 'age', ylabel ='weight', xlim =[15, 45], ylim= [0,15], legend = False)
```
