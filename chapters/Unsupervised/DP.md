<script type="text/javascript" async
    src="https://polyfill.io/v3/polyfill.min.js?features=es6">
</script>
<script type="text/javascript" async
    src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/3.2.0/es5/tex-mml-chtml.js">
</script>

# Data Preprocessing for Unsupervised Models

## The Indispensable Role of Feature Scaling

Data preprocessing is the first and most critical step in any machine
learning pipeline.15 Within unsupervised learning, feature scaling is an
indispensable part of this process, particularly for algorithms that
rely on distance calculations. The need for scaling arises from a common
challenge in real-world datasets: features often have different units
and ranges of magnitude. For example, a dataset for housing prices might
have features for “square footage” (in thousands) and “number of
bedrooms” (a small integer).

If such data is used directly in a distance-based algorithm, the feature
with the larger range—in this case, square footage—will
disproportionately influence the distance calculation, effectively
overshadowing other important features like the number of bedrooms. This
can lead to biased and misleading clustering results, as the algorithm
will primarily group data points based on the dominant feature,
regardless of the other variables. Scaling is the preventative measure
against this vulnerability. By transforming all features to a common
scale, it ensures that each variable contributes equally to the distance
metrics and, consequently, to the model’s outcome.16 The causal chain is
clear: disparate feature scales lead to skewed distance metrics, which
in turn produce suboptimal or nonsensical clusters. Scaling prevents
this by ensuring a fair and balanced contribution from all features,
which is essential for achieving accurate and reliable results.

## Normalization vs. Standardization

Two of the most common methods for feature scaling are normalization and
standardization, terms that are often used interchangeably but have
distinct meanings.

### Normalization

**Normalization**, often referred to as Min-Max scaling, rescales
feature values to a fixed range, typically between 0 and 1. It achieves
this by subtracting the minimum value of a feature and dividing by its
range (the difference between the maximum and minimum values). This
method is useful when the data is not normally distributed and the goal
is to preserve the relationships within the data while ensuring all
features are on a comparable scale.

$$
\large x\_{normalized}  = \frac{x\_{i} - x\_{min}}{x\_{max} - x\_{min}}
$$

### Standardization

**Standardization**, also known as Z-score normalization, transforms
data to have a mean of zero and a standard deviation of one. The process
involves subtracting the mean from each feature value and dividing by
the standard deviation. Standardization is vital for algorithms that
rely on variance or assume a **Gaussian distribution**, such as
Principal Component Analysis (PCA). The choice between the two methods
is not arbitrary; it is a higher-order decision dictated by the
assumptions of the algorithm being used and the inherent distribution of
the data. For instance, standardization is a prerequisite for PCA’s
mathematical assumptions to hold, demonstrating that preprocessing is
not a separate step but an integral part of the model’s foundation.

$$
\large z = \frac{(x\_{i} - \mu)}{\sigma}
$$

-   *x*<sub>*i*</sub> : *O**b**s**e**r**v**a**t**i**o**n**s*
-   *μ*: Mean
-   *σ*: Satndard deviation

### Robust Scaling

**Robust Scaling** is the technique that is actually robust to outliers.
It transforms data using the median and the interquartile range (IQR).
The formula is:

$$
\large x\_{robust} = \frac{(x -median)}{IQR}
$$

-   **Median**: The median is the middle value of a dataset. Unlike the
    mean, it is not affected by extreme values.
-   **Interquartile Range (IQR)**: The IQR is the range of the middle
    50% of the data, calculated as the difference between the 75th
    percentile (Q3) and the 25th percentile (Q1). Like the median, the
    IQR is resistant to outliers because it ignores the upper and lower
    25% of the data.

Because Robust Scaling uses these outlier-resistant metrics, it performs
well when a dataset contains extreme values. The outliers themselves are
still present in the transformed data, but their influence on the
scaling process is minimized. This is in contrast to standardization and
normalization, where outliers can significantly skew the entire
dataset’s scale
