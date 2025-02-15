# Machine Learning

Machine learning (ML) is like teaching a computer to learn from
experience, just like how humans learn. Imagine we want to teach a child
to recognize apples. We show them many pictures of apples and tell them,
“This is an apple.” Over time, the child becomes good at spotting apples
because they’ve learned from all the examples we have shown.

In machine learning, we do the same thing with computers. We feed them
lots of data (like pictures of apples) and tell them what it is. Over
time, the computer “learns” patterns from the data, and eventually, it
can make predictions or recognize things on its own.

For example, if we show it a new picture of fruit, it can say, “That’s
an apple” without us telling it. The more data the computer sees, the
better it gets at learning, just like a person practicing a skill.

The key thing is that the computer isn’t given exact instructions on how
to do something. Instead, it figures it out by looking at lots of
examples!

Machine learning can be divided into different types based on how the
computer learns from the data. The two main types are **supervised
learning** and **unsupervised learning**, and here’s an easy way to
understand them:

## 1. Supervised Learning

Supervised learning is like teaching with answers. Imagine we are
helping a child with a math worksheet, and we give them both the
questions and the correct answers. After doing enough practice, the
child learns how to solve similar math problems on their own.

In machine learning, this works the same way. The computer is given lots
of data with labels (the correct answers). For example, if we show the
computer pictures of cats and dogs, we also tell it which picture is a
cat and which is a dog. Over time, it learns to identify new pictures as
either a cat or a dog without needing the labels anymore. It’s like the
computer’s being supervised and guided with the correct answers until it
can make predictions on its own.

## 2. Unsupervised Learning

Unsupervised learning is like learning without any answers. Imagine a
group of kids playing with a set of blocks, but no one tells them how to
sort them. They have to figure it out themselves. Some kids might group
the blocks by color, others by size, and some by shape.

In this type of machine learning, the computer is given a lot of data
but no labels or answers. The computer has to figure out patterns or
group things on its own. For example, if we give it a bunch of pictures
without saying what they are, it might start grouping them based on
similarities, like sorting animals from cars without anyone telling it
what’s what. So, in short: \* **Supervised learning**: The computer is
taught with the right answers and learns to make predictions. •
**Unsupervised learning**: The computer has no answers and must find
patterns independently.

## Label vs Feature in a Machine Learning Dataset

### Label

In machine learning, a **label** is the answer or the correct result
that we want the computer to learn to predict. It’s like the name tag we
give to data so the computer knows what it represents.

### Features

In machine learning, **features** are the information or characteristics
that the computer examines to make a decision or prediction. Think of
features as clues or hints that help the computer understand the data.

#### Example

Imagine a bank is trying to predict whether or not a person will repay a
loan. The data could include information like the person’s income,
credit score, and loan amount. ID is just a unique label and will not be
part of final ML model. The label would be whether the person repaid the
loan or defaulted (didn’t repay).

**Bank loan example**

<table>
<thead>
<tr class="header">
<th style="text-align: left;">ID</th>
<th style="text-align: left;">Income</th>
<th style="text-align: left;">Credit Score</th>
<th style="text-align: left;">Loan amount</th>
<th style="text-align: left;">Loan Status</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">1051</td>
<td style="text-align: left;">50000</td>
<td style="text-align: left;">700</td>
<td style="text-align: left;">15000</td>
<td style="text-align: left;">Repaid</td>
</tr>
<tr class="even">
<td style="text-align: left;">1052</td>
<td style="text-align: left;">75000</td>
<td style="text-align: left;">450</td>
<td style="text-align: left;">20000</td>
<td style="text-align: left;">Defaulter</td>
</tr>
<tr class="odd">
<td style="text-align: left;">1053</td>
<td style="text-align: left;">80000</td>
<td style="text-align: left;">750</td>
<td style="text-align: left;">20000</td>
<td style="text-align: left;">Repaid</td>
</tr>
</tbody>
</table>

The **features** are the important details about each person that the
computer will use to make this prediction, like:

-   **Income**: How much money the person earns.
-   **Credit Score**: A number that represents how good their credit
    history is.
-   **Loan Amount**: The loan size the person is asking for.

These features help the computer `decide` if a person is likely to repay
the loan or not.

## Training and Test dataset

In **supervised machine learning**, the **training dataset** and **test
dataset** are like different stages of a learning process, just like
when we are preparing for an exam:

### 1. Training Dataset

The training dataset is like the study material we use to prepare for a
test. Imagine we are studying math, and we have a book with problems and
their correct answers. We practice solving those problems over and over
again, learning the rules and patterns. In machine learning, the
training dataset is a collection of examples (like pictures, numbers, or
sentences) along with the correct answers (called **labels**).

The computer uses the training data to **learn**. It looks at each
example and the correct label, and it figures out patterns. For example,
if we are teaching the computer to find a person will pay his loan or
not.

**Bank loan example**

<table>
<thead>
<tr class="header">
<th style="text-align: left;">ID</th>
<th style="text-align: left;">Income</th>
<th style="text-align: left;">Credit Score</th>
<th style="text-align: left;">Loan amount</th>
<th style="text-align: left;">Loan Status</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">1051</td>
<td style="text-align: left;">50000</td>
<td style="text-align: left;">700</td>
<td style="text-align: left;">15000</td>
<td style="text-align: left;">Repaid</td>
</tr>
<tr class="even">
<td style="text-align: left;">1052</td>
<td style="text-align: left;">75000</td>
<td style="text-align: left;">450</td>
<td style="text-align: left;">20000</td>
<td style="text-align: left;">Defaulter</td>
</tr>
<tr class="odd">
<td style="text-align: left;">1053</td>
<td style="text-align: left;">80000</td>
<td style="text-align: left;">750</td>
<td style="text-align: left;">20000</td>
<td style="text-align: left;">Repaid</td>
</tr>
<tr class="even">
<td style="text-align: left;">…</td>
<td style="text-align: left;">…</td>
<td style="text-align: left;">…</td>
<td style="text-align: left;">…</td>
<td style="text-align: left;">…</td>
</tr>
</tbody>
</table>

Here, training dataset contains not only information about features, but
also label (loan status).

### 2. Test Dataset

The test dataset is like the actual exam we take after studying. We
don’t have the answers here, and we’re expected to use what we learned
during practice to solve the questions. In machine learning, the test
dataset is a set of examples that the computer hasn’t seen before. The
difference is that it doesn’t come with the answers (at least not at
first). The idea is to see how well the computer **learned** from the
training data. We give it the test data, and it makes predictions based
on what it has learned. Then, we compare its predictions to the real
answers (which we kept hidden from the computer). If it does well, it
means the computer learned well. If it doesn’t, we might need to go back
and give it more training or adjust how it learned.

**Bank loan example**

<table>
<thead>
<tr class="header">
<th style="text-align: left;">ID</th>
<th style="text-align: left;">Income</th>
<th style="text-align: left;">Credit Score</th>
<th style="text-align: left;">Loan amount</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">3051</td>
<td style="text-align: left;">45000</td>
<td style="text-align: left;">770</td>
<td style="text-align: left;">10000</td>
</tr>
<tr class="even">
<td style="text-align: left;">3052</td>
<td style="text-align: left;">38000</td>
<td style="text-align: left;">480</td>
<td style="text-align: left;">15000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">3053</td>
<td style="text-align: left;">65000</td>
<td style="text-align: left;">720</td>
<td style="text-align: left;">20000</td>
</tr>
<tr class="even">
<td style="text-align: left;">…</td>
<td style="text-align: left;">…</td>
<td style="text-align: left;">…</td>
<td style="text-align: left;">…</td>
</tr>
</tbody>
</table>

Here, test dataset used in ML model contains only information about
features, but no information about label. Hence, using a specific ML
model we have to predict loan status. Though, during the whole process,
test dataset also contains label. But, while evaluating a model we
exclude label data. Once prediction is done, we compare predicted value
with actual value in test dataset to check if model is working well.
Once we are sure that model performed well, and then we can use the
model for new coming dataset.

In summary: \* **Training dataset**: Like practice questions with
answers. The computer learns from this data. \* **Test dataset**: Like a
test with new questions. The computer uses what it learned to make
predictions, and we check how well it did.

Supervised machine learning is further divided into two types, based on
**outcome/label** or **dependent** variable, **regression** and
**classification**. The difference between regression and classification
in machine learning is based on the kind of task the computer is doing —
predicting a number or categorizing something. Here’s an easy way to
understand them:
