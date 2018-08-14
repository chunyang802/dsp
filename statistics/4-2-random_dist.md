[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> REPLACE THIS TEXT WITH YOUR RESPONSE


          numbers = np.random.random(1000)
          numbers_pmf = thinkstats2.Pmf(numbers)
          thinkplot.Pmf(numbers_pmf,linewidth=0.1)
          thinkplot.Show(xlabel = 'random number', ylabel = 'pmf')

          numbers_cdf =thinkstats2.Cdf(numbers)
          thinkplot.Cdf(numbers_cdf)
          thinkplot.Show(xlabel = 'random number', ylabel ='CDF')
