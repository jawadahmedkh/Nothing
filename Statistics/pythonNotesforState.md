# 1. Measure of Central Tendency

## 1.1. **Mean**

```python
import numpy as np
from scipy import stats

data = [2, 4, 6]

# Arithmetic Mean
arithmetic_mean = np.mean(data)

# Geometric Mean
geometric_mean = stats.gmean(data)

# Harmonic Mean
harmonic_mean = stats.hmean(data)

print("Arithmetic Mean:", arithmetic_mean)
print("Geometric Mean:", geometric_mean)
print("Harmonic Mean:", harmonic_mean)
```
---

## 1.2. **Median and Mode**

```python
import numpy as np
from scipy import stats

data = [10, 20, 20, 30, 40, 50]

# Median
median_value = np.median(data)

# Mode
mode_value = stats.mode(data, keepdims=True).mode[0]

print("Mean:", mean_value)
print("Median:", median_value)
print("Mode:", mode_value)
```
---

# 2. Population Mean

```python
# Population Data (Entire group)
population_data = [15, 22, 34, 42, 50]

# Population Mean Formula
population_mean = sum(population_data) / len(population_data)

print("Population Mean (µ):", population_mean)
```

---

# 3. Sample Mean

```python
import random

# Sample Data (Subset of the population)
sample_data = random.sample(population_data, 3)  # Randomly pick 3 values from population

# Sample Mean Formula
sample_mean = sum(sample_data) / len(sample_data)

print("Sample Mean (x̄):", sample_mean)
```
---

# 4. Range 


```python
import numpy as np
# Example Data
data = [15, 22, 34, 42, 50]

# Range
data_range = max(data) - min(data)

#            OR

data_range = np.ptp(data)


print("Range:", data_range)
```

---

# 5. Population Standard Deviation

```python
# Example Data
data = [15, 22, 34, 42, 50]

population_std_dev = np.std(data)

print("Population Standard Deviation:", population_std_dev)
```
---

# 6. Population Variance

```python
# Example Data
data = [15, 22, 34, 42, 50]

population_variance = np.var(data)

print("Population Variance:", population_variance)
```
---

# 7. Sample Standard Deviation

```python
# Example Data
data = [15, 22, 34, 42, 50]

sample_std_dev = np.std(data, ddof=1)   # ddof=1 for sample

print("Sample Standard Deviation:", sample_std_dev)
```
---

# 8. Sample Variance

```python
# Example Data
data = [15, 22, 34, 42, 50]

sample_variance = np.var(data, ddof=1)  # ddof=1 for sample

print("Sample Variance:", sample_variance)
```

---

# 9. IQR

```python
# Example Data
data = [15, 22, 34, 42, 50]

# Interquartile Range (IQR)
Q1 = np.percentile(data, 25)
Q3 = np.percentile(data, 75)
IQR = Q3 - Q1
print("Interquartile Range (IQR):", IQR)
```

OR

```python
from scipy.stats import iqr

# Sample dataset
data = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])

# Calculate Interquartile Range (IQR) using scipy
iqr_value = iqr(data)

print("Interquartile Range (IQR):", iqr_value)
```

---

# 10. Skewness

```python
import scipy.stats as stats
skewness = stats.skew(data)
```

---

# 11. Kurtosis

```python
import scipy.stats as stats
kurtosis = stats.kurtosis(data)
```

---

# 11. 