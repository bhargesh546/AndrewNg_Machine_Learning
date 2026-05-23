
**Machine learning** <br>
                    "Field of study that gives computers the ability 
                    to learn without being explicitly programmed."
                                            Arthur Samuel (1959)

Two Types - <br> 
    1. Supervised <br>
    2. Unsupervised <br>
    3. Recommender System <br>
    4. Reinforcement Learning <br>

1. Supervised<br>
    i. Regression - Predict numbers out of infinitely many possible numbers. <br> 
    ii. Classification - Only finite possible outcomes/categories. Here a boundary line is made to differentiate the outcomes using the algorithm<br>

2. Unsupervised <br>
    i. Clustering - Grouping similar data points together <br>
    ii. Anomaly detection - Detects unusual events or data points<br>
    iii. Dimensionality reduction - Compress dataset


**1.i. Regression**

For linear function (single variable/independent variable).
This is the $\hat{y}$ value

<center>f<sub>(w,b)</sub>(x) = wx + b</center>

We can adjust parameters w and b to improve our model

>Q. But how do we find values of w and b such that the straight line fit or our estimated prediction is closer to the true value of y 

For this we use the Cost Function (Squared Error Cost Function) where we compare the
$\hat{y}$ to y 


$$ J^{(w,b)} = \frac{1}{2m} \sum_{i = 1}^{m}(\hat{y}^{(i)} - y^{i})^{2} $$

So we would like to minimize the value of J as small as possible as a function of w and b
i.e.  $$\underset{w,b} {\text{minimize}} J(w, b)$$

Gradient Descent Algorithm - To minimize any function and other cost functions with one or more parameters.
> **Note:** for some functions there can be more than one minimum and the shape may not be convex bell.

Here we update the value w to 
$$w = w - \alpha \frac{\delta}{\delta w} J(w, b)$$

$$b = b - \alpha \frac{\delta}{\delta b} J(w, b)$$

where $\alpha$ = learning rate i.e. a small positive number between 0 and 1. It determines how big step (size) we are taking downhill. Determines the efficiency (slow or fast)

The derivative term determines in which direction we want to take the step.

So that finally we can converge it 

Batch Gradient Descent - Here at each step of the gradient descent we are using all the training examples instead of a subset of the training data


**Multiple Linear Regression -** Here there are multipie features that determines the output value.
$$f_{\vec{w}, b}(\vec{x}) = w_1x_1 + w_2x_2 +... + w_nx_n + b $$

<center>OR</center> 

$$f_{\vec{w}, b}(\vec{x}) = \vec{\mathbf{w}}.\vec{\mathbf{x}} + b$$