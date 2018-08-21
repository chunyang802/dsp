[Think Stats Chapter 6 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2007.html#toc60) (household income)

>> 
```python
import numpy as np
import hinc
import thinkstats2
import thinkplot
df = hinc.ReadData()

df['log_upper'] = np.log10(df.income)
df['log_lower'] = df.log_upper.shift(1)
df.loc[0, 'log_lower'] = 3.0
df.loc[41, 'log_upper'] = 6.0

arrays =[]
for _, row in df.iterrows():
    vals = np.linspace(row.log_lower, row.log_upper, row.freq)
    arrays.append(vals)

sample_log = np.concatenate(arrays)
sample = np.power(10, sample_log)

sample_cdf = thinkstats2.Cdf(sample)
thinkplot.Cdf(sample_cdf)
thinkplot.Show(xlabel = 'income', ylabel = 'CDF')

sample_mean = Mean(sample)
sample_median = Median(sample)
skewness = Skewness(sample)
pearsonmedianskewness= PearsonMedianSkewness(sample)
below_mean = cdf.Prob(sample_mean)
below_mean
```
The percentage of household that has income below the mean depends on the assumption that the upper limit of the income is 1 million. Apparently, if the upper limit is higher, say 10 million, there will be a higher percentage of household income that fall below the mean. 
