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
*f* : *X* → *Y*
