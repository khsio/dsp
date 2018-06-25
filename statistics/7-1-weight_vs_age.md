[Think Stats Chapter 7 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2008.html#toc70) (weight vs. age)

#import nessesary package  
import first

#setting up data  
live, firsts, others = first.MakeFrames()  
live = live.dropna(subset=['agepreg', 'totalwgt_lb'])  

#plotting weight vs age
thinkplot.Scatter(live.agepreg, live.totalwgt_lb, alpha=0.1, s=10)  
thinkplot.Config(xlabel="Mother's Age (year)",  
                 ylabel="Birth Weight (lbs)",  
                 legend=False)  

#binning age before plotting precentile birth weight vs age
bins = np.arange(10, 48, 3)  
indices = np.digitize(live.agepreg, bins)  
groups = live.groupby(indices)  

ages = [group.agepreg.mean() for i, group in groups][1:-1]  
cdfs = [thinkstats2.Cdf(group.totalwgt_lb) for i, group in groups][1:-1]  

for percent in [75, 50, 25]:  
    weights = [cdf.Percentile(percent) for cdf in cdfs]  
    label = '%dth' % percent  
    thinkplot.Plot(ages, weights, label=label)  

#plotting precentile weight vs age
thinkplot.Config(xlabel="Mother's age (years)",  
                ylabel='Birth weight (lbs)',  
                xlim=[14, 45], legend=True)  

#computing Pearson's correlation  
Corr(live.totalwgt_lb, live.agepreg)  
0.0688339703541091  

#computing Spearman's correlation
SpearmanCorr(live.totalwgt_lb, live.agepreg)  
0.09461004109658226  

#Conclusion  
1. From the plot of weight vs age, it is hard to tell the relationship  
2. From the plot of precentile weight vs age, you can tell there is probability no strong relationship between two variables  
3. From both correlation coefficient, we can confirm that there is not much correlation between two variables  