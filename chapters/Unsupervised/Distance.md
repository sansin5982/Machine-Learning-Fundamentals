<script type="text/javascript" async
    src="https://polyfill.io/v3/polyfill.min.js?features=es6">
</script>
<script type="text/javascript" async
    src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/3.2.0/es5/tex-mml-chtml.js">
</script>

# The Mathematical Foundation: Distance and Proximity

## 2.1. The Role of Distance and Similarity Measures

At the core of many unsupervised machine learning algorithms,
particularly those used for clustering, are mathematical concepts known
as distance and similarity measures. These measures are not mere
technical details; they are fundamental components that quantify the
similarity or dissimilarity between two data points in a
multi-dimensional space. By defining how “close” or “far apart”
different data points are, these metrics directly influence how an
algorithm groups them into clusters.

The selection of a distance measure is a critical modeling decision that
encodes a researcher’s assumptions about the data’s inherent structure.
The chosen metric defines the geometry of the problem and will, as a
result, strongly influence the shape of the clusters that are
discovered. For a clustering solution to be meaningful, the distance
metric must align with the type and properties of the data being
analyzed. A mismatch between the metric and the data’s true geometry can
lead to suboptimal or nonsensical clusters, making this one of the most
important choices in a clustering pipeline.

## 2.2. Key Distance and Similarity Metrics

A variety of distance and similarity metrics are available, each suited
for different types of data and specific use cases. The following table
and explanations detail some of the most common ones.

#### Table 2: Key Distance and Similarity Metrics

<table>
<colgroup>
<col style="width: 10%" />
<col style="width: 30%" />
<col style="width: 19%" />
<col style="width: 39%" />
</colgroup>
<thead>
<tr>
<th>Metric</th>
<th>Formula</th>
<th>Data Type Suitability</th>
<th>Ideal Use Case</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Euclidean Distance</strong></td>
<td>$d(x,y) = $)</td>
<td>Continuous variables</td>
<td>The default for many algorithms; measures straight-line distance in
a continuous space.</td>
</tr>
<tr>
<td><strong>Manhattan Distance</strong></td>
<td>$d(x,y) = _{i=1}^n</td>
<td>x_i - y_i</td>
<td>$)</td>
</tr>
<tr>
<td><strong>Minkowski Distance</strong></td>
<td>$d_m = (_{i=1}^n</td>
<td>x_i - y_i</td>
<td><sup>m)</sup>{1/m} $)</td>
</tr>
<tr>
<td><strong>Jaccard Similarity</strong></td>
<td>$ $)</td>
<td>Binary or binarized data</td>
<td>Determining the similarity and diversity of two sample sets.</td>
</tr>
<tr>
<td><strong>Cosine Similarity</strong></td>
<td>$ = $)</td>
<td>High-dimensional or text data</td>
<td>Used when vector direction is more important than magnitude (e.g.,
text analysis, recommendation engines).</td>
</tr>
</tbody>
</table>

-   **Euclidean Distance** is the most widely used distance metric and
    is often the default choice in many machine learning libraries. It
    calculates the straight-line distance between two points in
    n-dimensional space, based on the Pythagorean theorem. While
    intuitive, it has significant drawbacks: it is not scale-invariant,
    meaning features with larger magnitudes can disproportionately
    influence the distance. It is also less effective in
    high-dimensional spaces, a phenomenon known as the curse of
    dimensionality, where the distance between any two points converges
    to a constant value, making differentiation difficult.

-   **Manhattan Distance**, also known as the “city block” or “taxicab”
    distance, calculates the distance by summing the absolute
    differences along each dimension. It is particularly useful for data
    that can be viewed on a grid-like structure, such as street networks
    or binary data. Unlike Euclidean distance, it does not consider
    diagonal distances.

-   The **Minkowski metric** provides a generalization of both Euclidean
    and Manhattan distances. It is defined by a parameter, p, where
    setting p=1 yields Manhattan distance and p=2 yields Euclidean
    distance. This flexibility allows a data scientist to tune the
    metric based on the specific problem’s spatial relationships.

-   **Jaccard Similarity** is a metric designed to calculate the
    similarity of two sets of data. It is particularly effective for
    binary or binarized data, as it measures the size of the
    intersection of the two sets relative to their union.

-   Finally, **Cosine Similarity** measures the cosine of the angle
    between two vectors. This metric is useful in high-dimensional
    spaces where the magnitude of the vectors is less important than
    their orientation. It is commonly applied in text analysis to
    determine document similarity based on word frequency, where two
    documents might be of different lengths but are considered similar
    if the angle between their term vectors is small.
