[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>>
```python
      import scipy.stats
      male_height_distribution = scipy.stats.norm(loc = 178, scale = 7.7)

      height_1 = (5*12+10)*2.54
      height_2 = (6*12+1)*2.54

      percentage = male_height_distribution.cdf(height_2) - male_height_distribution.cdf(height_1)
      percentage
```
