1-Model Architecture
# Maintainers

	a)-Convolutional Layers: Key for feature extraction, these layers apply various filters to the input images to create feature maps that represent different aspects of the images.
Activation Functions: ReLU (Rectified Linear Unit) is used after each convolutional layer to introduce non-linearities into the model, making it capable of learning complex patterns.
Batch Normalization: Implemented following each convolutional layer to stabilize and accelerate the training process by normalizing the activations.
Dropout Layers: Included to prevent overfitting by randomly dropping units (along with their connections) during the training phase.
Pooling Layers: Utilized to reduce the spatial dimensions of the feature maps, thereby decreasing the computational load and minimizing the risk of overfitting.
Global Average Pooling (GAP): Applied before the final layer to reduce each feature map to a single value, effectively summarizing the essential information.
Fully Connected Layer: The network concludes with a fully connected layer that maps the reduced features to the output classes.
Depthwise Separable Convolutions: Learned the importance of using depthwise separable convolutions for reducing the model's parameter count without sacrificing the ability to extract meaningful features from images.
Channel and Layer Optimization: Gained insights into balancing the number of channels and layers to manage model complexity and ensure efficiency.
Adaptive Pooling: Understood the utility of adaptive pooling in ensuring consistent output sizes, which is crucial for aligning the model's output with classification layers.

2-Training Procedure

Loss Function: Cross-entropy loss is used, suitable for multi-class classification problems.
Optimizer: Adam optimizer is chosen for its efficiency in converging towards the optimal weights.
Learning Rate Scheduler: A strategy to adjust the learning rate over epochs, improving the model's ability to find the optimal solution.

3-Regularization:
Dropout and Batch Normalization: Confirmed the effectiveness of dropout in preventing overfitting, and recognized the role of batch normalization in stabilizing training.

4-Data Augmentation: 
Albumentations Library: Explored the Albumentations library for advanced image augmentation techniques, appreciating its flexibility and effectiveness in enhancing model generalization.
We implemented following using Albumentations Library-
horizontal flip
shiftScaleRotate
coarseDropout (max_holes = 1, max_height=16px, max_width=16, min_holes = 1, min_height=16px, min_width=16px, fill_value=(mean of your dataset), mask_fill_value = None)

5-Training Strategies
Learning Rate Optimization: Acknowledged the importance of learning rate scheduling and adjustments to improve model convergence and performance.
Impact of Augmentation: Investigated how different data augmentation strategies can significantly affect model accuracy and robustness.

6-Accuracy: 
Measures the proportion of correctly classified images.

7-Challenges Encountered
Balancing the model's depth and width within the parameter constraints posed a significant challenge, requiring careful architectural planning.
Ensuring the receptive field exceeded 44 while maintaining or improving model accuracy involved strategic adjustments to convolution and pooling layers.



