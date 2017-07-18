## Training Neural Network

### Part 1
- Activation Functions
- Data Preprocessing
- Weight Initialization
- Batch Normalization
- Babysitting the Learning Process
- Hyperparameter Optimization

#### Activation Functions
1.Sigmoid  
$\sigma (x) = \frac{1}{1+e^{-x}}$

problems:  
 - 1 . Saturated neurons 'kill' the gradients

 - 2 . Sigmoid outputs are not zero-centered

 - 3 . exp() is a bit compute expensive

2.tanh  
$tanh(x) = 2 \times \sigma (x)$

still kill gradients with saturated

3.ReLU  
$ReLU(x) = max(0, x)$

 - 1 . Does not saturate
 - 2 . Very computationally efficient
 - 3 . Converge much faster
 - 4 . more biologically plausible

problem:  
not zero-centered output

4.Leaky ReLU  
$max(0.1x, x)$
 - 1 . Does not saturate
 - 2 . Computationally efficient
 - 3 . Converges much faster
 - 4 . will not 'die'

5.Maxout  
$max(w_1^T x + b_1, w_2^T x + b_2)$

Generalizes ReLU and Leaky ReLU

6.ELU
$\begin{cases} x \quad x\geq 0 \\ \alpha (e^x - 1) \quad x \leq 0 \end{cases}$

 - 1 . All benefits of ReLU
 - 2 . Closer to zero mean outputs
 - 3 . Negative saturation regime compared with Leaky ReLU, adds some robustness to noise

In practice:
- Use ReLU. Be careful with your learning rates  
- Try out Leaky ReLU / Maxout / ELU  
- Try out tanh but don't expect much
- Don't use sigmoid

#### Data Preprocessing

**Step 1**:Preprocessing the data  
original data --> zero-centered data --> normalized data

PCA and Whitening of the data  

In practice for Images: center only  
- Subtract the mean image
- Subtract per-channel mean

#### Weight Initialization
- First idea: Small random numbers  
Works okay for small networks, but problems with deeper networks

- Xavier Initialization  
```python
W = np.random.randn(fan_in, fan_out) / np.sqrt(fan_in)
```
but when using the ReLU nonlinearity it breaks

- He(note additonal /2)  
```python
W = np.random.randn(fan_in, fan_out) / np.sqrt(fan_in/2)
```

#### Batch Normalization
1.Compute the empirical mean and variance independently for each dimension

2.Usually inserted after Fully Connected or Convolutional layers, and before nonlinearity

3.at test time BatchNorm layer will use a single fixed empirical mean during training

Loss not going down:  
Learning rate is too low

Loss exploding:  
Learning rate is too high
