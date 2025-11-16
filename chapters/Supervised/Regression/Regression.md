# Regression

**Regression** is a type of **supervised machine learning** technique
used to **predict a continuous numerical output (dependent variable)**
based on one or more **input features (independent variables)**.

> Given a dataset
> *D* = {(*x*<sub>1</sub>, *y*<sub>1</sub>), (*x*<sub>2</sub>, *y*<sub>2</sub>), …, (*x*<sub>*n*</sub>, *y*<sub>*n*</sub>)},
> where *x*<sub>*i*</sub> ∈ ℝ<sup>*d*</sup> (input features) and
> *y*<sub>*i*</sub> ∈ ℝ (continuous target), regression learns a
> function *f*(*x*) such that
> *f*(*x*<sub>*i*</sub>) ≈ *y*<sub>*i*</sub>, minimizing prediction
> error.

## What is Regression?

Regression answers **“How much?”** or **“What will be the value?”** It
models the **relationship between variables** to make **quantitative
predictions**.

-   **Input**: Numerical or categorical features
-   **Output**: A real number (e.g., 250.5, -10.2, 98.6)
-   **Goal**: Minimize difference between predicted and actual values
    (using loss functions like MSE)

### Real-Life Applications of Regression

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr>
<th style="text-align: left;">Industry</th>
<th style="text-align: left;">Application</th>
<th style="text-align: left;">Example</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;">Finance</td>
<td style="text-align: left;">Stock price prediction</td>
<td style="text-align: left;">Predict tomorrow’s share price using past
trends</td>
</tr>
<tr>
<td style="text-align: left;">Real Estate</td>
<td style="text-align: left;">House price estimation</td>
<td style="text-align: left;">“Predict price from size, location,
age”</td>
</tr>
<tr>
<td style="text-align: left;">Healthcare</td>
<td style="text-align: left;">Patient recovery time</td>
<td style="text-align: left;">Estimate hospital stay duration</td>
</tr>
<tr>
<td style="text-align: left;">Marketing</td>
<td style="text-align: left;">Sales forecasting</td>
<td style="text-align: left;">Predict next quarter revenue</td>
</tr>
<tr>
<td style="text-align: left;">Weather</td>
<td style="text-align: left;">Temperature prediction</td>
<td style="text-align: left;">Forecast temperature 24 hours ahead</td>
</tr>
<tr>
<td style="text-align: left;">E-commerce</td>
<td style="text-align: left;">Demand prediction</td>
<td style="text-align: left;">Estimate product demand during
festivals</td>
</tr>
</tbody>
</table>
