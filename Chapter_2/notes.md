## Chapter 2: Statistical Learning

### 2.1 What is statistical learning?

***Statistical learning*** refers to a set of approaches for estimating $f$. 
$$Y=f(X)+\epsilon$$
Here $f$ is some fixed but unknown function of different ***predictors***, $X_1,X_2, \ldots, X_p,$ and $\epsilon$ is a random error term, which is independent of $X$ and has mean zero. In this formulation, $f$ represents the systematic information that $X$ provides about ***response*** $Y$.

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

##### &#10148; Inference



#### 2.1.2 How Do We Estimate $f$?





