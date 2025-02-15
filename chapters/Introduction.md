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

# Label vs Feature in a Machine Learning Dataset

## Label

In machine learning, a **label** is the answer or the correct result
that we want the computer to learn to predict. It’s like the name tag we
give to data so the computer knows what it represents.

## Features

In machine learning, **features** are the information or characteristics
that the computer examines to make a decision or prediction. Think of
features as clues or hints that help the computer understand the data.

### Example

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
