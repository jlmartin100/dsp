[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

## Python Code:

```python
CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)

print(firsts.totalwgt_lb.std(), others.totalwgt_lb.std()
```

## Output:

-0.088672927072602

This is larger than the computed Cohen effect size for first pregnancy length, which was 0.028879044654449883. It is also still considerably smaller than the respective standard deviations within the `firsts` and `others` data.
