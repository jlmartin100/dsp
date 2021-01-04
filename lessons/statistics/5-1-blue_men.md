[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>In the BRFSS (see Section 5.4), the distribution of heights is roughly normal with parameters µ = 178 cm and σ = 7.7 cm for men, and µ = 163 cm and σ = 7.3 cm for women.
In order to join Blue Man Group, you have to be male between 5’10” and 6’1” (see http://bluemancasting.com). What percentage of the U.S. male population is in this range? Hint: use scipy.stats.norm.cdf.

#### Use the BRFSS parameters and scipy.stats.norm to create the distribution of heights in centimeters for the U.S. male population
```python
mu = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mu, scale=sigma)
```
#### Check the distribution against the parameters given
```python
dist.mean(), dist std()
```
(178.0, 7.7)

#### Convert given measurements
```python
# 5'10" = 70"
# 1 inch = 2.54 cm
print(f"5 ft 10 in equals {70 * 2.54} cm")
```
5 ft 10 in equals 177.8 cm

```python
# 6'1" = 73" 
print(f"6 ft 1 in equals {73 * 2.54} cm")
```
6 ft 1 in equals 185.42000000000002 cm

#### Use converted measurements to establish the lower and upper bounds of the CDF
```python
lower = dist.cdf(177.8)
higher = dist.cdf(185.42)
```

#### Calculate the percentage within the bounds
```python
print(f"The percentage of the U.S. male population in the height range for the Blue Man Group is {higher - lower}.")
```
The percentage of the U.S. male population in the height range for the Blue Man Group is 0.3427468376314737.
