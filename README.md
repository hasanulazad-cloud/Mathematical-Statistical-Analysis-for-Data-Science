# 📐 Mathematical & Statistical Analysis for Data Science

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hasanulazad-cloud/Mathematical-Statistical-Analysis-for-Data-Science/blob/main/Mathematical_%26_Statistical_Analysis_for_Data_Science.ipynb)
![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Linear%20Algebra-013243?logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-Statistics-8CAAE6?logo=scipy&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

> The maths behind data science, in code: **linear algebra**, **probability**, **Bayes' theorem**, **probability distributions** and **descriptive statistics**, implemented with NumPy and SciPy.

---

## 📌 Project Overview

Machine learning rests on a small set of mathematical ideas. This project works through each one with a concrete example, so the formulas are tied to real numbers: matrices and eigenvalues, the chance of a successful sale, how Bayes' theorem updates a belief, and what the shape of a dataset says about it.

---

## 📂 Repository Contents

| File | Description |
|---|---|
| `Mathematical_&_Statistical_Analysis_for_Data_Science.ipynb` | Full notebook with all tasks and outputs (opens in Google Colab via the badge above) |

---

## 🧩 Topics Covered

### 1️⃣ Linear Algebra (NumPy)
- Vector addition, subtraction and dot product
- Matrix addition and multiplication
- Determinant, with the inverse computed only when the determinant is non-zero
- Eigenvalues and eigenvectors

### 2️⃣ Probability
- Probability of a successful sale, with a Bernoulli simulation
- Conditional probability by customer segment (Premium and Regular)
- Bayes' theorem

### 3️⃣ Probability Distributions
- **Binomial:** number of successes in 20 trials
- **Normal:** 1,000 samples with mean 50 and standard deviation 10
- **Uniform:** 1,000 samples between 0 and 1

### 4️⃣ Descriptive Statistics
- Central tendency: mean, median, mode
- Dispersion: range, variance, standard deviation
- Shape: skewness and kurtosis

---

## 📊 Key Results

### Linear algebra

| Operation | Result |
|---|---|
| Vector addition | `[3, 7, 11]` |
| Vector subtraction | `[1, 1, 1]` |
| Dot product | `44` |
| Determinant of `matrix_a` | 6 (non-zero, so the inverse exists) |
| Eigenvalues of `matrix_a` | 5.54, −2.00, −0.54 |

### Probability

| Measure | Value |
|---|---|
| P(successful sale) | 0.65 |
| P(Purchase given Premium) | 0.80 |
| P(Purchase given Regular) | 0.50 |
| **P(Premium given Purchase), by Bayes** | **0.5161 (51.61%)** |

> 💡 **Bayes in plain words:** Premium customers are only 40% of all customers, but they make up about **52% of all purchases**, because they buy more often.
> The inputs are consistent: 0.40 × 0.80 + 0.60 × 0.50 = 0.62, which matches the P(Purchase) used.

### Distributions

| Distribution | Setting | Result |
|---|---|---|
| Binomial | n = 20, p = 0.65 | Mean 13.0, variance 4.55 (equal to n·p and n·p·(1−p)) |
| Normal | mean 50, SD 10 | Sample mean ≈ 50.3, sample SD ≈ 9.9 |
| Uniform | 0 to 1 | Sample mean ≈ 0.50 |

The sample statistics sit close to the theoretical values, which is the law of large numbers at work.

### Descriptive statistics of 20 sales figures

| Statistic | Value |
|---|---|
| Mean | 165.5 |
| Median | 165 |
| Mode | 135, 145, 155, 165, 175 (five-way tie) |
| Range | 90 |
| Variance | 534.75 |
| Standard deviation | 23.12 |
| Skewness | 0.03 |
| Kurtosis (excess) | −0.71 |

**Reading it:** mean and median almost match and skewness is close to zero, so the sales are roughly **symmetric**. Negative kurtosis means a flatter distribution with lighter tails than a normal curve.

---

## 🚀 How to Run

**Option 1: Google Colab.** Click the *Open in Colab* badge at the top.

**Option 2: Locally**

```bash
# 1. Clone the repository
git clone https://github.com/hasanulazad-cloud/Mathematical-Statistical-Analysis-for-Data-Science.git
cd Mathematical-Statistical-Analysis-for-Data-Science

# 2. Install the dependencies
pip install numpy scipy pandas jupyter

# 3. Open the notebook
jupyter notebook "Mathematical_&_Statistical_Analysis_for_Data_Science.ipynb"
```

---

## ⚠️ Known Limitations

- **Skewness label is too strong.** The code prints "Positively Skewed" for any value above zero, including 0.03. A tolerance (for example, call it symmetric when |skew| is under 0.5) would be more accurate.
- **Random results change on every run.** The Bernoulli, binomial, normal and uniform samples have no seed, so the sampled numbers differ each time. `np.random.seed(42)` makes them repeatable.
- **Conditional probabilities are given, not derived.** Task 2 prints the supplied values for Premium and Regular rather than computing them from data.
- **Population variance.** `np.var` divides by n; use `ddof=1` for the sample variance (562.9 for this data).

---

## 🔮 Future Improvements

- Plot the distributions (histograms with theoretical curves overlaid)
- Add hypothesis testing and confidence intervals
- Add correlation and covariance
- Apply the same tools to a real dataset

---

## 👤 Author

**Hasanul H Azad**
Medical billing / RCM professional upskilling in Data Science, AI and Machine Learning
GitHub: [@hasanulazad-cloud](https://github.com/hasanulazad-cloud)

---

⭐ If you found this useful, consider starring the repo.
