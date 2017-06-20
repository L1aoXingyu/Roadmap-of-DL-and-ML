## 5神经网络

### 5.1神经元模型
神经网络是具有适应性的简单单元组成的广泛并行互连的网络

### 5.2感知机与多层网络
感知机(Perceptron)有两层神经元组成，能够容易地实现逻辑与、或、非运算。

感知机的输出为 $\hat{y}$，权重可以这么调整

$$w_i \leftarrow w_i + \Delta w_i$$

$$\Delta w_i = \eta (y-\hat{y})x_i$$

$\eta$称为学习率(learning rate)
