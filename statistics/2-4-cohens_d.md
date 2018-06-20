[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

firsts = live[live.birthord == 1]\
others = live[live.birthord != 1]

firsts.totalwgt_lb.mean(), others.totalwgt_lb.mean()
(7.201094430437772, 7.325855614973262)\
#firsts babies are lgither than others in average

CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb), CohenEffectSize(firsts.prglngth, others.prglngth)\
(-0.088672927072602, 0.028879044654449883)\
#the effect of size of totalwgt_lb is higher than prglngth, but still very small
