[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

Downey has already broken out the original pregnancy data frames into two distinct data frames, the first born, and the not first born.  `live` is the dataframe of all rows in which there was a live birth.

```python
firsts = live[live.birthord == 1]
others = live[live.birthord != 1]
```
The Cohen Effect Size function, found in the textbook, allows us to calculate the Cohen Effect Size for the total weight of first born babies and other babies.

#### Python Code:

```python
print("Cohen effect size for first births vs other births: ", CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb))

print("Standard deviation within first births data: ", firsts.totalwgt_lb.std())
print("Standard deviation within other births data: ", others.totalwgt_lb.std())
```

#### Output:

Cohen effect size for first births vs other births:  -0.088672927072602
Standard deviation within first births data:  1.4205728777207374
Standard deviation within other births data:  1.3941954762143138

This is larger than the computed Cohen effect size for first pregnancy length as noted in the book, which was 0.028879044654449883. It is also still considerably smaller than the respective standard deviations within the `firsts` and `others` data.  So the variability of weights within the first born data and within the others data is greater than the Cohen Effect Size of the difference between the two groups.
