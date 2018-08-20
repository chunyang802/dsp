[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>>   
```python
def CohentEffectSize(group1,group2):
      diff = group1.mean()-group2.mean()
      var1 = group1.var()
      var2 = group2.var()
      n1,n2 = len(group1),len(group2)
      pooled_var = (n1*var1+n2*var2)/(n1+n2)
      pooled_std = math.sqrt(pooled_var)
      d = diff/pooled_std
 preg = nsfg.ReadFemPreg()
 live = preg[preg.outcome == 1]
 firsts = live[live.birthord == 1]
 others = live[live.birthord !=1]
 birth_weight_diff = CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
 pregnancy_length_diff = CohenEffectSize(firsts.prglngth, others.prglngth)
 ```
