[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

num = np.random.random(1000)  
num_pmf = thinkstats2.Pmf(num, label="num")  
thinkplot.Pmf(num_pmf, linewidth=0.1)  
thinkplot.Config(xlabel='num', ylabel='PMF')  

num_cdf = thinkstats2.Cdf(num)  
thinkplot.cdf(num_cdf)  
thinkplot.Config(xlabel="num", ylabel="CDF")  

#both PMF and CDF are uniform in this case
