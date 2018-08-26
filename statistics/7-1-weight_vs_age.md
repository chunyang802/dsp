[Think Stats Chapter 7 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2008.html#toc70) (weight vs. age)

>> 
First to generate a scatter plot to see how weight varies with age
```python
import first

live, firsts, others = first.MakeFrames()
live = live.dropna(subset=['agepreg', 'totalwgt_lb'])
age = live.agepreg
weights = live.totalwgt_lb
thinkplot.Scatter(age, weights, alpha = 1.0)
thinkplot.Config(xlabel = 'age', ylabel ='weight', xlim =[15, 45], ylim= [0,15], legend = False)
```
Then calculate correlatioin 
```python
Corr(age, weights)
SpearmanCorr(age, weights)
```
Bin the preganancy age, and group the weight by the bins. Plot the weight percentile vs. the age. 
```python
bins = np.arange(10,48,3)
indices = np.digitize(age,bins)
groups = live.groupby(indices)

age_1 = [group.agepreg.mean() for i, group in groups][1:-1]
cdfs = [thinkstats2.Cdf(group.totalwgt_lb) for i, group in groups][1:-1]

thinkplot.PrePlot(3)
for percent in [75,50,25]:
    weight = [cdf.Percentile(percent) for cdf in cdfs]
    label = '%dth'%percent
    thinkplot.Plot(age_1, weight, label = label)
    
thinkplot.Config(xlabel = 'mother age', ylabel = 'weight', xlim = [10,48], legend = True)
```
