## Loss Functions and Optimization
@(CS231n)

### Linear Classifier:
TODO:  

1.Define a loss function that quantifies scores

2.Come up with a way of efficiently finding the parameters that minimize the loss function(**optimization**)

**loss function**:  
A loss function tells how good our current classifier is

Given a dataset of examples $\{(x_i, y_i)\}_{i=1}^N$

where $x_i$ is image and $y_i$ is (integer) label

Loss over the dataset is a sum of loss over examples:
$$L = \frac{1}{N}\sum_i L_i(f(x_i, W), y_i)$$

#### Multiclass SVM loss:
Given $(x_i, y_i)$, $s = f(x_i, W)$

SVM loss:  
$$L_i = \sum_{j \neq y_i}max(0, s_j - s_{y_i} + 1)$$

**Regularization**

1. $L^2 = \sum_k \sum_l w_{k, l}^2$

2. $L^1 = \sum_k \sum_l |w_{k, l}|$

3. Elastic net ($L_1 + L_2$)

4. Max norm regularizaiton

5. Dropout

6. Fancier: Batch normalization, stochastic depth  

$$R(w) = \sum_k \sum_l W_{k, l}^2$$

$$L = \frac{1}{N} \sum_i L_i + \lambda R(W)$$

#### Softmax classifier
$$L_i = -log(\frac{e^{f_{y_1}}}{\sum_j e^{f_j}})$$

$$P(y_i | x_i; W) = \frac{e^{f_{y_i}}}{\sum_j e^{f_j}}$$
$y_i$ is the real label

want to maximum the probability

**Practical issues: Numeric stability**

exponentials are large numbers and dividing large numbers can be numerically unstable.

**Trick**:  
multiply the top and bottom of the fraction by a constant C and push it into the sum, set $log C = -max_j f_j$
![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3623720-03a6c33ef2dd99f7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### Optimization
Strategy 1. Random search

Strategy 2. Following the Gradient

Negative gradient is the steepest descend direction

#### Computing the gradient
1. numerical gradient  
slow, approximate but easy

2. analytic gradient  
fast, exact but more error-prone

**Mini-batch gradient descent**
In large -scale applications, the training data can have on order of millions of examples. A very common way is computing a batches of training data gradient. This is called Stochastic Gradient Descent(SGD).
