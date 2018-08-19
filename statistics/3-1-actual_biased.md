[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> 
  resp = nsfg.ReadFemResp()**
  pmf = thinkstats2.Pmf(resp.numkdhh, label = 'actual')**
  def BiasedPmf(pmf, label = 'Biased'):**
  new_pmf = pmf.Copy (label = label)**
  for x, p in pmf.Items():**
  new_pmf.Mult(x,x)**
  new_pmf.Normalize()**
  return new_pmf**
  biased_pmf = BiasedPmf(pmf, label = 'Biased')**
  thinkplot.PrePlot(2)**
  thinkplot.Pmfs([pmf,biased_pmf])**
  thinkplot.Show(xlabel = 'kid_number', ylabel = 'probability')**
