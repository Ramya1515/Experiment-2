# Experiment-2
Computes descriptive statistics and empirical probabilities using Pandas and NumPy.
AIM:
 Compute descriptive statistics and empirical probabilities; generate samples from
distributions.
ALGORITHM (brief):
 Use pandas.Series for statistics; numpy.random for sampling.
PROGRAM:
import numpy as np
import pandas as pd
heights = np.array([160,165,170,175,180,155,168,172,169,158])
s = pd.Series(heights)
print("Mean:", s.mean())
print("Median:", s.median())
print("Std dev:", round(s.std(),3))
print("Variance:", round(s.var(),3))
print("P(height > 170):", (s>170).mean())
sample = np.random.normal(loc=s.mean(), scale=s.std(), size=10)
print("Random sample (10) from normal around mean:",
np.round(sample,2))
DETAILED EXPLANATION:
1. import numpy as np & import pandas as pd — load libraries.
2. heights — a NumPy array of sample heights.
3. s = pd.Series(heights) — create pandas Series for convenience.
4. .mean(), .median(), .std(), .var() — compute descriptive stats.
5. (s>170).mean() — boolean mask then mean to compute empirical probability.
6. np.random.normal(...) — draw synthetic samples (for simulation/bootstrapping).
SAMPLE OUTPUT :
Mean: 168.2
Median: 169.0
P(height > 170): 0.4
Random sample (10) from normal around mean: [170.3 166.2 173.1 ...]
RESULT:
 Students learn central tendency, spread, and simple empirical probability estimation.
THEORY:
 Descriptive statistics and sampling basics used throughout ML.
Std dev: 7.756
Variance: 60.17
