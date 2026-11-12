## AIM

Compute descriptive statistics and empirical probabilities; generate samples from distributions.

## ALGORITHM (Brief)

Use `pandas.Series` for statistics; `numpy.random` for sampling.

## PROGRAM

```
import numpy as npimport pandas as pdheights = np.array([160,165,170,175,180,155,168,172,169,158])s = pd.Series(heights)print("Mean:", s.mean())print("Median:", s.median())print("Std dev:", round(s.std(),3))print("Variance:", round(s.var(),3))print("P(height > 170):", (s>170).mean())sample = np.random.normal(loc=s.mean(), scale=s.std(), size=10)print("Random sample (10) from normal around mean:",      np.round(sample,2))
```

## DETAILED EXPLANATION

1. import numpy as np & import pandas as pd – Loads the NumPy and Pandas libraries for numerical operations and statistical calculations.
2. heights – Creates a NumPy array containing sample height values.
3. s = pd.Series(heights) – Converts the NumPy array into a Pandas Series for convenient statistical calculations.
4. .mean(), .median(), .std(), .var() – Calculate the mean, median, standard deviation and variance of the height values.
5. (s>170).mean() – Uses a Boolean condition to identify heights greater than 170 and calculates their empirical probability.
6. np.random.normal(...) – Generates ten random samples from a normal distribution using the calculated mean and standard deviation.

## SAMPLE OUTPUT

```
Mean: 168.2
Median: 169.0
Std dev: 7.756
Variance: 60.178
P(height > 170): 0.4

Random sample (10) from normal around mean:
[170.3 166.2 173.1 ...]
```

## RESULT

Students learn central tendency, spread, and simple empirical probability estimation.

## THEORY

Descriptive statistics and sampling basics are used throughout Machine Learning.
