<script type="text/javascript" async
    src="https://polyfill.io/v3/polyfill.min.js?features=es6">
</script>
<script type="text/javascript" async
    src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/3.2.0/es5/tex-mml-chtml.js">
</script>

# Supervised Machine Learning

**Supervised Machine Learning** is a subset of machine learning where an
algorithm is trained on a **labeled dataset**, meaning each input data
point is paired with a corresponding correct output (label). The goal is
to learn a mapping function from inputs to outputs so that the model can
predict the output for new, unseen data accurately.

Formally:

Given a dataset
*D* = (*x*<sub>1</sub>, *y*<sub>1</sub>), (*x*<sub>2</sub>, *y*<sub>2</sub>), ..., (*x*<sub>*n*</sub>, *y*<sub>*n*</sub>),
where *x*<sub>*i*</sub> is the input feature vector and
*y*<sub>*i*</sub> is the target label, the algorithm learns a function
*f* : *X* → *Y* that minimizes prediction error.

## What is Supervised Machine Learning?

It is a **learning paradigm** where the model is “supervised” by
providing both **input features** and correct output labels during
training. The model adjusts its internal parameters to reduce the
difference between its predictions and the actual labels (using a loss
function). After training, it can make predictions on new data.

Think of it like teaching a child with flashcards: you show an image
(input) and tell them the answer (label: “cat”). Over time, they learn
to identify cats on their own.

### Applications

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr>
<th style="text-align: left;">Domain</th>
<th style="text-align: left;">Application</th>
<th style="text-align: left;">Example</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;">Healthcare</td>
<td style="text-align: left;">Disease prediction</td>
<td style="text-align: left;">“Predicting diabetes from blood sugar,
BMI, age”</td>
</tr>
<tr>
<td style="text-align: left;">Finance</td>
<td style="text-align: left;">Credit scoring,“Approving loans based on
income</td>
<td style="text-align: left;">credit history”</td>
</tr>
<tr>
<td style="text-align: left;">Retail</td>
<td style="text-align: left;">Customer churn prediction</td>
<td style="text-align: left;">Predicting if a user will stop using a
service</td>
</tr>
<tr>
<td style="text-align: left;">Automotive</td>
<td style="text-align: left;">Spam email detection</td>
<td style="text-align: left;">“Classifying emails as”spam” or “not
spam”</td>
</tr>
<tr>
<td style="text-align: left;">Autonomous Vehicles</td>
<td style="text-align: left;">Object detection</td>
<td style="text-align: left;">Identifying pedestrians in camera
images</td>
</tr>
</tbody>
</table>

#### Example (House Price prediction)

Predict house prices based on size, bedrooms, and location.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr>
<th style="text-align: left;">Size (sqft)</th>
<th style="text-align: left;">Bedrooms</th>
<th style="text-align: left;">Location_Score (1–10)</th>
<th style="text-align: left;">Price (in $1000s) (Target Label)</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;">1500</td>
<td style="text-align: left;">3</td>
<td style="text-align: left;">8</td>
<td style="text-align: left;">300</td>
</tr>
<tr>
<td style="text-align: left;">2200</td>
<td style="text-align: left;">4</td>
<td style="text-align: left;">9</td>
<td style="text-align: left;">450</td>
</tr>
<tr>
<td style="text-align: left;">1800</td>
<td style="text-align: left;">3</td>
<td style="text-align: left;">7</td>
<td style="text-align: left;">320</td>
</tr>
<tr>
<td style="text-align: left;">2600</td>
<td style="text-align: left;">5</td>
<td style="text-align: left;">10</td>
<td style="text-align: left;">600</td>
</tr>
<tr>
<td style="text-align: left;">1200</td>
<td style="text-align: left;">2</td>
<td style="text-align: left;">6</td>
<td style="text-align: left;">220</td>
</tr>
</tbody>
</table>

-   **Input Features (X)**: Size, Bedrooms, Location\_Score
-   **Output Label (y)**: Price
-   **Task**: Regression (predict continuous value)

### Types of Supervised Machine Learning

Supervised ML is mainly divided into two types based on the nature of
the target variable:

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr>
<th style="text-align: left;">Type</th>
<th style="text-align: left;">Description</th>
<th style="text-align: left;">Output Type</th>
<th style="text-align: left;">Example Algorithms</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;">1. Classification</td>
<td style="text-align: left;">Predicts a <strong>discrete class label
(category)</strong>. The output belongs to a finite set of classes.</td>
<td style="text-align: left;">“Categorical (e.g., Yes/No, Cat/Dog)”</td>
<td style="text-align: left;">“Logistic Regression, Decision Trees, SVM,
Random Forest, Neural Networks”</td>
</tr>
<tr>
<td style="text-align: left;">2. Regression</td>
<td style="text-align: left;">Predicts a <strong>continuous numerical
value</strong>. The output can be any real number.</td>
<td style="text-align: left;">“Numerical (e.g., price,
temperature)”</td>
<td style="text-align: left;">“Linear Regression, Polynomial Regression,
Ridge/Lasso, SVR, Gradient Boosting”</td>
</tr>
</tbody>
</table>

### Classification

-   **Goal**: Assign input to one of predefined categories.
-   **Evaluation**: Accuracy, Precision, Recall, F1-Score, Confusion
    Matrix.
-   **Example**: Identifying if a tumor is malignant or benign from
    medical images.

#### Email Spam Classification

<table>
<thead>
<tr>
<th style="text-align: left;">Word Count</th>
<th style="text-align: left;">Has Free</th>
<th style="text-align: left;">From Known Domain</th>
<th style="text-align: left;">Label (Spam = 1, Not Spam = 0)</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;">45</td>
<td style="text-align: left;">Yes</td>
<td style="text-align: left;">No</td>
<td style="text-align: left;">1</td>
</tr>
<tr>
<td style="text-align: left;">120</td>
<td style="text-align: left;">No</td>
<td style="text-align: left;">Yes</td>
<td style="text-align: left;">0</td>
</tr>
<tr>
<td style="text-align: left;">30</td>
<td style="text-align: left;">Yes</td>
<td style="text-align: left;">No</td>
<td style="text-align: left;">1</td>
</tr>
</tbody>
</table>

200,No,Yes,0

### Regression

-   **Goal**: Predict a quantity.
-   **Evaluation**: Mean Squared Error (MSE), R² Score, MAE.
-   **Example**: Forecasting stock prices or temperature based on
    historical trends.

#### House Price prediction

Predict house prices based on size, bedrooms, and location.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr>
<th style="text-align: left;">Size (sqft)</th>
<th style="text-align: left;">Bedrooms</th>
<th style="text-align: left;">Location_Score (1–10)</th>
<th style="text-align: left;">Price (in $1000s) (Target Label)</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;">1500</td>
<td style="text-align: left;">3</td>
<td style="text-align: left;">8</td>
<td style="text-align: left;">300</td>
</tr>
<tr>
<td style="text-align: left;">2200</td>
<td style="text-align: left;">4</td>
<td style="text-align: left;">9</td>
<td style="text-align: left;">450</td>
</tr>
<tr>
<td style="text-align: left;">1800</td>
<td style="text-align: left;">3</td>
<td style="text-align: left;">7</td>
<td style="text-align: left;">320</td>
</tr>
<tr>
<td style="text-align: left;">2600</td>
<td style="text-align: left;">5</td>
<td style="text-align: left;">10</td>
<td style="text-align: left;">600</td>
</tr>
<tr>
<td style="text-align: left;">1200</td>
<td style="text-align: left;">2</td>
<td style="text-align: left;">6</td>
<td style="text-align: left;">220</td>
</tr>
</tbody>
</table>

### Difference Between Regression and Classification

<table>
<thead>
<tr>
<th>Feature</th>
<th>Regression</th>
<th>Classification</th>
</tr>
</thead>
<tbody>
<tr>
<td>Output Type</td>
<td>Numeric/continuous</td>
<td>Categorical/discrete</td>
</tr>
<tr>
<td>Example</td>
<td>Predict price</td>
<td>Predict spam/ham</td>
</tr>
<tr>
<td>Algorithms</td>
<td>Linear Regression</td>
<td>Logistic Regression</td>
</tr>
</tbody>
</table>
