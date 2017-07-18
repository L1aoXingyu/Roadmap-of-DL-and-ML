## Lecture 2
@(CS231n)

## Image Classification: A core task in Computer Vision

### Challenges:
- lllumination
- Deformation
- Occlusion
- Background Clutter
- Intraclass variation

### Data-Driven Approach
```python
def train(images, labels):
  # Machine learning!
  return model
```

```python
def predict(model, test_images):
  # Use model to predict labels
  return test_labels
```

### First classifier: Nearest Neighbor

1. Memorize all data and labels

2. Predict the label of the most similar training image

**Distance Metric**:  
L1 distance: $d_1(I_1, I_2) = \sum_{p} |I_1^p - I_1^p|$  
L2 distance: $d_2(I_1, I_2) = \sqrt(\sum_p(I_1^p - I_2^p)^2)$

With N examples, train is O(1), and predict is O(N), this is bad because We want to predicting fast and slow for training is ok.

**K-Nearest Neighbors**:  
Instead of copying label from nearest neighbor, take majority vote from K closest points

**Hyperparameters**:  
What is the best value of K ?  
What is the best distance to use ?

*Idea1*:  
Split data into train, val and test; choose hyperparameters on val and evaluate on test  

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3623720-4cdee0d95cdc68cc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

*Idea2*:Cross-Validation  
Split data into folds, try each fold as validation and average the results  
Useful for small datasets, but not used too frequently in deep learning


![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3623720-ab51b66f52b1e4b7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

K-Nearest Neighbor on images **never used**:  
- Very slow at test time  
- Distance metrics on pixels are not informative

### K-Nearest Summary
The K-Nearest Neighbors classifier predicts labels based on nearest training examples  

Distance metric and K are hyperparameters  

Choose hyperparameters using the validation set

### Parametric Approach: Linear Classification

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3623720-3ffbc732b961b6ae.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
