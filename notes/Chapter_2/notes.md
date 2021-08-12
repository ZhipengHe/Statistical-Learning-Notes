## Chapter 2: Statistical Learning

### 2.1 What is statistical learning?

***Statistical learning*** refers to a set of approaches for estimating $f$. 
$$Y=f(X)+\epsilon$$
Here $f$ is some fixed but unknown function of different ***predictors***, $X_1,X_2, \ldots, X_p,$ and $\epsilon$ is a random error term, which is independent of $X$ and has mean zero. In this formulation, $f$ represents the systematic information that $X$ provides about ***response*** $Y$.

<br>

#### 2.1.1 Why Estimate $f$?

##### &#10148; Prediction

A set of inputs $X$ are readily available, but the output $Y$ cannot be easily obtained. We can predict $Y$ using 
$$\hat Y=\hat f(X),$$
where $\hat f$ represents our estimate for f, and $\hat Y$ represents the resulting prediction for Y. In this setting, $\hat f$ is often treated as a ***black box***, in the sense that one is not typically concerned with the exact form of $\hat f$, provided that it yields accurate predictions for $Y$.

The accuracy of $\hat Y$ as a prediction for $Y$ depends on two quantities,
which we will call the ***reducible error*** and the ***irreducible error***.

- The reducible error is reducible because we can potentially improve the accuracy of $\hat Y$ by using the most appropriate statistical learning technique to estimate $f$.
- For the irreducible error, even if it were possible to form a perfect estimate for $f$, so that our estimated response took the form $\hat Y = f(X)$, our prediction would still have some error in it! 
  - This is because $Y$ is also a function of $\epsilon$, which, by definition, cannot be predicted using $X$. Therefore, variability associated with $\epsilon$ also affects the accuracy of our predictions. This is known as the irreducible error, because no matter how well we estimate $f$, we cannot reduce the error introduced by $\epsilon$.

Consider a given estimate $\hat Y$ and a set of predictors $X$, which yields the prediction $\hat Y=\hat f(X)$. Assume for a moment that both $\hat f$ and $X$ are fixed, so that the only variability comes from $\epsilon$. Then, it is easy to show that
$$E(Y- \hat Y)^2 = E[f(X)+\epsilon- \hat f(X)]^2
= [f(X)- \hat f(X)]^2+ Var(\epsilon),$$
where $E(Y- \hat Y)^2$ represents the average, or ***expected value***, of the squared difference between the predicted and actual value of $Y$, and $Var(\epsilon)$ represents the ***variance*** associated with the error term $\epsilon$.

<br>

##### &#10148; Inference

Different from prediction, inference is aimed at understanding the association between $Y$ and $X_1, \ldots, X_p$. In this situation we wish to estimate $f$, but our goal is not necessarily to make predictions for $Y$. Now $\hat f$ cannot be treated as a black
box, because we need to know its exact form.

<br>

##### &#10148; Prediction & Inference

Some modeling could be conducted both for prediction and inference. Depending on whether our ultimate goal is prediction, inference, or a combination of the two, different methods for estimating $f$ may be appropriate.

<br>

#### 2.1.2 How Do We Estimate $f$?

##### &#10148; Parametric Methods

Parametric methods involve a two-step model-based approach.

1. First, we make an assumption about the functional form, or shape, of $f$. For example, one very simple assumption is that $f$ is linear in $X$:
$$f(X)=\beta_0 +\beta_1 X_1+\beta_2 X-2 +\ldots+\beta_p X_p$$
Once we have assumed that f is linear, the problem of estimating $f$ is greatly simplified. Instead of having to estimate an entirely arbitrary $p$-dimensional function $f(X)$, one only needs to estimate the $p + 1$ coefficients $\beta_1+\beta_2+\ldots+\beta_p$.

2. After a model has been selected, we need a procedure that uses the training data to ***fit*** or train the model. In the case of the linear model, we need to estimate the parameters $\beta_1+\beta_2+\ldots+\beta_p$. That is, we want to find values of these parameters such that
$$Y \approx \beta_0 +\beta_1 X_1+\beta_2 X-2 +\ldots+\beta_p X_p$$

The model-based approach just described is referred to as ***parametric***; it reduces the problem of estimating $f$ down to one of estimating a set of parameters. 

***Advantages***: 

- ***Simpler***: Assuming a parametric form for $f$ simplifies the problem of estimating $f$ because it is generally much easier to estimate a set of parameters than to fit an entirely arbitrary function $f$.
- ***Speed***: Parametric models are very fast to learn from data.
- ***Less Data***: They do not require as much training data and can work well even if the fit to the data is not perfect.

***Disadvantages***:

- ***Constrained***: By choosing a functional form these methods are highly constrained to the specified form.
- ***Limited Complexity***: The methods are more suited to simpler problems.
- ***Poor Fit***: The chosen model will usually not match the true unknown form of $f$.

***Examples***: 

- Linear Regression
- Logistic Regression
- Perceptron
- Naive Bayes
- Simple Neural Networks

<br>

##### &#10148; Non-Parametric Methods

Non-parametric methods do not make explicit assumptions about the functional form of $f$. Instead they seek an estimate of f that gets as close to the data points as possible without being too rough or wiggly.

***Advantages***:

- ***Flexibility***: Capable of fitting a large number of functional forms.
- ***Power***: No assumptions (or weak assumptions) about the underlying function.
- ***Performance***: Can result in higher performance models for prediction.

***Disadvantages***:

- ***More data***: Require a lot more training data to estimate the mapping function.
- ***Slower***: A lot slower to train as they often have far more parameters to train.
- ***Overfitting***: More of a risk to overfit the training data and it is harder to explain why specific predictions are made.

***Examples***:

- k-Nearest Neighbors
- Support Vector Machine
- Random Forests

<br>

#### 2.1.3 Prediction Accuracy and Model Interpretability



<br>

#### 2.1.4 Supervised Versus Unsupervised Learning


<br>

#### 2.1.5 Regression Versus Classification Problems


<br>


### Reference

[1] [An Introduction to Statistical Learning: with Applications in R, Second Edition](https://www.statlearning.com/), Chapter 2

[2] [Parametric and Nonparametric Machine Learning Algorithms](https://machinelearningmastery.com/parametric-and-nonparametric-machine-learning-algorithms/), Blog Post



