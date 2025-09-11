# 1 The Foundational Vocabulary of Machine Learning

Understanding machine learning requires a grasp of its foundational
terminology. These concepts are the building blocks of any ML project,
and their relationships form a clear, systematic process. Building an
effective model is not a one-time event but a cyclical process of
building, testing, and refining.

## 1.1 The Data: Features and Labels

Machine learning models learn from data that is structured into two
primary components: **features** and **labels**.

### 1.1.1 Label

In machine learning, a **label** is the answer or the correct result
that we want the computer to learn to predict. It’s like the name tag we
give to data so the computer knows what it represents.

### 1.1.2 Features

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
<tr>
<th style="text-align: left;">ID</th>
<th style="text-align: left;">Income</th>
<th style="text-align: left;">Credit Score</th>
<th style="text-align: left;">Loan amount</th>
<th style="text-align: left;">Loan Status</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;">1051</td>
<td style="text-align: left;">50000</td>
<td style="text-align: left;">700</td>
<td style="text-align: left;">15000</td>
<td style="text-align: left;">Repaid</td>
</tr>
<tr>
<td style="text-align: left;">1052</td>
<td style="text-align: left;">75000</td>
<td style="text-align: left;">450</td>
<td style="text-align: left;">20000</td>
<td style="text-align: left;">Defaulter</td>
</tr>
<tr>
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

## 1.2 The Building Blocks: Algorithms and Models

The distinction between an algorithm and a model is a fundamental
concept.

## 1.2.1 Algorithm

An **algorithm** is like a set of instructions or a recipe that tells
the computer how to solve a problem. Imagine you’re baking a cake. You
follow a recipe with steps like mixing ingredients, baking at a certain
temperature, and decorating. The recipe is the **algorithm** a
step-by-step process to get the final result (the cake).

In machine learning, an algorithm is the method or process the computer
uses to learn from the data. For example, in the case of linear
regression, the algorithm tells the computer how to find the best-fit
line that predicts outcomes.

## 1.2.2 Model

A **model** is the final product after the computer has finished
learning from the data using the algorithm. In the baking example, the
cake is the model. Once you’ve followed the recipe, the end result is
something you can eat and use. In machine learning, the model is what
the computer creates after learning from the data. It’s the tool that
makes predictions or decisions. For instance, if you’ve trained the
computer to predict house prices based on house size and location, the
model is what you use to input new house data and get a predicted price.

#### Summary:

-   **Algorithm**: The set of instructions (or recipe) the computer
    follows to learn from the data.
-   **Model**: The end result (or the cake!) that the computer builds
    after using the algorithm to learn from the data, which can then be
    used to make predictions.

So, the algorithm is how the computer learns, and the model is what the
computer uses to make future predictions based on that learning.

------------------------------------------------------------------------

## 1.3 Types of Machine Learning

### 1.3.1 Supervised Learning

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

Supervised machine learning is further divided into two types, based on
**outcome/label** or **dependent** variable, **regression** and
**classification**. The difference between regression and classification
in machine learning is based on the kind of task the computer is doing —
predicting a number or categorizing something. Here’s an easy way to
understand them:

#### 1.3.1.1 Regression

Regression is about predicting a number, like guessing someone’s age or
estimating the price of a house. Imagine we’re trying to predict how
much a house costs based on things like its size, location, and number
of bedrooms. The task here is to predict a specific number — the price
of the house.

In machine learning, regression is used when the computer is asked to
predict a **continuous value** (a number). For example, if we want the
computer to predict the temperature for tomorrow based on historical
weather data, that’s a regression task because the output is a number
(the temperature).

Let’s use an example of house price prediction, which is a common
regression problem. In this case, the goal is to predict the price of a
house (the outcome) based on certain features like the size of the house
and the number of bedrooms.

Here’s an example of how the training dataset and test dataset might
look:

#### Training dataset (Used to train the ML model)

<table>
<thead>
<tr>
<th style="text-align: left;">House size (sq ft)</th>
<th style="text-align: left;">Number of bedrooms</th>
<th style="text-align: left;">Price (label)</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;">1500</td>
<td style="text-align: left;">3</td>
<td style="text-align: left;">3000000</td>
</tr>
<tr>
<td style="text-align: left;">2000</td>
<td style="text-align: left;">4</td>
<td style="text-align: left;">4000000</td>
</tr>
<tr>
<td style="text-align: left;">1800</td>
<td style="text-align: left;">3</td>
<td style="text-align: left;">3300000</td>
</tr>
<tr>
<td style="text-align: left;">2500</td>
<td style="text-align: left;">5</td>
<td style="text-align: left;">5500000</td>
</tr>
<tr>
<td style="text-align: left;">1200</td>
<td style="text-align: left;">2</td>
<td style="text-align: left;">2700000</td>
</tr>
</tbody>
</table>

This is where the machine learns from the data, which includes both the
features (house size, number of bedrooms) and the correct answers (house
prices).

#### Test dataset (Used to test how well the model predicts)

<table>
<thead>
<tr>
<th style="text-align: left;">House size (sq ft)</th>
<th style="text-align: left;">Number of bedrooms</th>
<th style="text-align: left;">Actual Price</th>
<th style="text-align: left;">Predicted Price</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;">1700</td>
<td style="text-align: left;">3</td>
<td style="text-align: left;">3450000</td>
<td style="text-align: left;">340000</td>
</tr>
<tr>
<td style="text-align: left;">2200</td>
<td style="text-align: left;">4</td>
<td style="text-align: left;">4200000</td>
<td style="text-align: left;">410000</td>
</tr>
<tr>
<td style="text-align: left;">1400</td>
<td style="text-align: left;">2</td>
<td style="text-align: left;">2550000</td>
<td style="text-align: left;">260000</td>
</tr>
</tbody>
</table>

After training, we test the model on new data. It only sees the features
(house size, number of bedrooms), as we remove actual price from the
test data. When model is ready we check how well it predicts the price
compared to the actual price. If prediction is close we can use new
dataset without label. If there is a difference in actual price and
predicted price, we alter parameters to improve the model.

#### 1.3.1.2 Classification

Classification is about putting things into categories, like sorting
objects into boxes. Imagine we have a bunch of fruits, and we want to
sort them into two boxes: one for apples and one for oranges. The task
is to decide which fruit goes into which box.

In machine learning, classification is when the computer is given some
data and asked to predict which **category** it belongs to. For example,
if we are teaching a computer to recognize emails as either “spam” or
“not spam,” that’s a classification task. The computer looks at an email
and decides which category (spam or not spam) it belongs to.

Let’s use a **bank loan approval** example for classification. The goal
is to predict whether a loan will be **approved** or **rejected** based
on features like income, credit score, and loan amount.

Here’s an example of how the training dataset and test dataset might
look:

#### Training dataset (Used to train the machine learning model)

<table>
<thead>
<tr>
<th>ID</th>
<th>Income</th>
<th>Credit Score</th>
<th>Loan Amount</th>
<th>Loan Status</th>
</tr>
</thead>
<tbody>
<tr>
<td>3051</td>
<td>45000</td>
<td>770</td>
<td>10000</td>
<td>Approved</td>
</tr>
<tr>
<td>3052</td>
<td>38000</td>
<td>480</td>
<td>15000</td>
<td>Rejected</td>
</tr>
<tr>
<td>3053</td>
<td>65000</td>
<td>720</td>
<td>20000</td>
<td>Approved</td>
</tr>
<tr>
<td>3054</td>
<td>25000</td>
<td>520</td>
<td>16000</td>
<td>Rejected</td>
</tr>
<tr>
<td>3055</td>
<td>42000</td>
<td>650</td>
<td>7000</td>
<td>Accepted</td>
</tr>
</tbody>
</table>

This is where the machine learns from the data, which includes the
features (income, credit score, loan amount) and the correct loan status
(approved or rejected).

#### Test Dataset

<table>
<colgroup>
<col style="width: 8%" />
<col style="width: 11%" />
<col style="width: 19%" />
<col style="width: 18%" />
<col style="width: 18%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr>
<th>ID</th>
<th>Income</th>
<th>Credit Score</th>
<th>Loan Amount</th>
<th>Loan Status</th>
<th>Predicted Status</th>
</tr>
</thead>
<tbody>
<tr>
<td>7051</td>
<td>38000</td>
<td>710</td>
<td>7500</td>
<td>Approved</td>
<td>Approved</td>
</tr>
<tr>
<td>7052</td>
<td>38000</td>
<td>480</td>
<td>15000</td>
<td>Rejected</td>
<td>Rejected</td>
</tr>
<tr>
<td>7053</td>
<td>65000</td>
<td>720</td>
<td>20000</td>
<td>Approved</td>
<td>Approved</td>
</tr>
</tbody>
</table>

After training, we test the model on new data. The model predicts the
loan status (approved or rejected), and we compare the predictions to
the actual loan status to see how well the model performed.

#### Summary:

• Classification: The computer puts things into categories (e.g., is
this a cat or a dog? Is this spam or not spam?). • Regression: The
computer predicts a number (e.g., what will the temperature be tomorrow?
How much will this house cost?).

So, classification deals with labels or categories, and regression deals
with numbers.

### 1.3.2 Unsupervised Learning

Unsupervised learning is like learning without any answers. Imagine a
group of kids playing with a set of blocks, but no one tells them how to
sort them. They have to figure it out themselves. Some kids might group
the blocks by color, others by size, and some by shape.

In this type of machine learning, the computer is given a lot of data
but no labels or answers. The computer has to figure out patterns or
group things on its own. For example, if we give it a bunch of pictures
without saying what they are, it might start grouping them based on
similarities, like sorting animals from cars without anyone telling it
what’s what.

### 1.3.3 Reinforcement Learning

Reinforcement learning is like learning by trial and error with rewards
and punishments. Imagine training a dog: when it sits on command, you
give it a treat (reward). If it does something wrong, you don’t give a
treat (no reward). Over time, the dog learns what actions lead to
rewards and avoids actions that don’t.

In machine learning, the computer (called an agent) interacts with an
environment and tries different actions. For each action, it gets
feedback (reward or penalty). The goal is to maximize the total reward.
For example, a self-driving car learns how to drive safely by getting
“rewards” for staying in the lane and penalties for crossing lines.

### 1.3.4 Semi-Supervised Machine Learning

Semi-supervised learning is like learning with just a few answers and
figuring out the rest. Imagine you’re in a class where the teacher only
solved a few math problems on the board but left the rest unsolved.
Using the solved ones as examples, you try to figure out the unsolved
ones on your own.

In machine learning, this means the computer is given a small set of
labeled data (with answers) and a large set of unlabeled data (without
answers). It uses the labeled examples to understand the patterns and
then applies that knowledge to the unlabeled data. For example, in
medical imaging, only a few X-rays may be labeled as “disease” or
“healthy” by doctors, and the computer uses those labeled examples to
learn, then classifies the rest of the X-rays on its own.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 28%" />
<col style="width: 36%" />
<col style="width: 23%" />
</colgroup>
<thead>
<tr>
<th>Learning Type</th>
<th>Key Idea</th>
<th>Analogy</th>
<th>Example Applications</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Supervised Learning</strong></td>
<td>Learns from labeled data (input + correct output).</td>
<td>A student learning with an answer key provided.</td>
<td>Spam filtering, credit scoring, disease diagnosis</td>
</tr>
<tr>
<td><strong>Unsupervised Learning</strong></td>
<td>Finds hidden patterns in unlabeled data.</td>
<td>Kids grouping blocks by color/shape without instructions.</td>
<td>Market segmentation, recommendation engines, anomaly detection</td>
</tr>
<tr>
<td><strong>Reinforcement Learning</strong></td>
<td>Learns by trial and error, using rewards and penalties.</td>
<td>Training a dog with treats and commands.</td>
<td>Self-driving cars, gaming AI, dynamic pricing</td>
</tr>
<tr>
<td><strong>Semi-Supervised Learning</strong></td>
<td>Uses a small amount of labeled data + a large amount of unlabeled
data.</td>
<td>A teacher solving a few math problems, students solve the rest by
themselves.</td>
<td>Medical imaging, text classification, speech recognition</td>
</tr>
</tbody>
</table>

## 1.4 Training and Test dataset

In **supervised machine learning**, the **training dataset** and **test
dataset** are like different stages of a learning process, just like
when we are preparing for an exam:

### 1.4.1 Training Dataset

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
<tr>
<th style="text-align: left;">ID</th>
<th style="text-align: left;">Income</th>
<th style="text-align: left;">Credit Score</th>
<th style="text-align: left;">Loan amount</th>
<th style="text-align: left;">Loan Status</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;">1051</td>
<td style="text-align: left;">50000</td>
<td style="text-align: left;">700</td>
<td style="text-align: left;">15000</td>
<td style="text-align: left;">Repaid</td>
</tr>
<tr>
<td style="text-align: left;">1052</td>
<td style="text-align: left;">75000</td>
<td style="text-align: left;">450</td>
<td style="text-align: left;">20000</td>
<td style="text-align: left;">Defaulter</td>
</tr>
<tr>
<td style="text-align: left;">1053</td>
<td style="text-align: left;">80000</td>
<td style="text-align: left;">750</td>
<td style="text-align: left;">20000</td>
<td style="text-align: left;">Repaid</td>
</tr>
<tr>
<td style="text-align: left;">…..</td>
<td style="text-align: left;">…..</td>
<td style="text-align: left;">…..</td>
<td style="text-align: left;">…..</td>
<td style="text-align: left;">…..</td>
</tr>
</tbody>
</table>

Here, training dataset contains not only information about features, but
also label (loan status).

### 1.4.2. Test Dataset

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
<tr>
<th style="text-align: left;">ID</th>
<th style="text-align: left;">Income</th>
<th style="text-align: left;">Credit Score</th>
<th style="text-align: left;">Loan amount</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;">3051</td>
<td style="text-align: left;">45000</td>
<td style="text-align: left;">770</td>
<td style="text-align: left;">10000</td>
</tr>
<tr>
<td style="text-align: left;">3052</td>
<td style="text-align: left;">38000</td>
<td style="text-align: left;">480</td>
<td style="text-align: left;">15000</td>
</tr>
<tr>
<td style="text-align: left;">3053</td>
<td style="text-align: left;">65000</td>
<td style="text-align: left;">720</td>
<td style="text-align: left;">20000</td>
</tr>
<tr>
<td style="text-align: left;">…..</td>
<td style="text-align: left;">…..</td>
<td style="text-align: left;">…..</td>
<td style="text-align: left;">…..</td>
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

In summary:

-   **Training dataset**: Like practice questions with answers. The
    computer learns from this data.

-   **Test dataset**: Like a test with new questions. The computer uses
    what it learned to make predictions, and we check how well it did.

## 1.5 Common Pitfalls: Overfitting and Underfitting

When a model is trained, it can encounter two common problems related to
its performance. **Overfitting** occurs when a model learns the training
data too well, including any noise and random fluctuations. An
overfitted model performs exceptionally well on the data it has already
seen but poorly on new, unseen data because it has essentially memorized
the training examples rather than learning the underlying, generalizable
patterns. An analogy for this is a student who memorizes test answers
instead of learning the core concepts; they will fail a new version of
the test.

On the other hand, **underfitting** happens when a model is too simple
to capture the underlying patterns in the data. As a result, it performs
poorly on both the training data and new data because it hasn’t learned
enough to make accurate predictions. An underfitted model is like a
student who hasn’t studied at all and fails the test completely.

## 1.6 Guiding the Process: Hyperparameters

When building a model, a practitioner must set certain configurations
called **hyperparameters**. Unlike a model’s parameters, which are
learned from the data during training, hyperparameters are settings that
are chosen before training begins and guide the learning process itself.
Examples include the learning rate (how much the model’s weights are
updated in each step) or the number of layers in a neural network. The
choice of hyperparameters can have a significant impact on the model’s
performance, and finding the optimal settings is a key part of the
machine learning workflow.

The relationship between these terms forms a cohesive, cyclical process.
An **algorithm** is trained on **features** and **labels** to produce a
model. The model’s quality is then evaluated for signs of
**overfitting** or **underfitting**, and a practitioner can adjust the
hyperparameters or perform other data preparation steps to refine the
model. This cyclical, iterative process of building, testing, and
refining is a core characteristic of practical machine learning work.
