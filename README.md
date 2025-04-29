Baseline: LeNet vs CustomCNN Comparison
----------------------------------------

Input:
- LeNet: 28x28 grayscale image, 1 channel
- CustomCNN: 28x28 grayscale image, 1 channel
- (Same input size)

Convolution Layers:
- LeNet: 2 Conv layers
- CustomCNN: 2 Conv layers
- (Both have 2 conv layers but with different configurations)

Channels:
- LeNet: 6 → 16
- CustomCNN: 32 → 64
- (CustomCNN has more channels to capture richer features)

Kernel Size:
- LeNet: 5x5
- CustomCNN: 3x3 (with padding=1)
- (CustomCNN uses smaller kernels for finer feature extraction)

Activation Function:
- LeNet: Tanh
- CustomCNN: ReLU
- (ReLU speeds up training and prevents vanishing gradients)

Pooling:
- LeNet: Average Pooling (AvgPool2d)
- CustomCNN: Max Pooling (MaxPool2d)
- (MaxPooling better preserves important features)

Dropout:
- LeNet: None
- CustomCNN: Dropout (0.25 after conv, 0.5 after FC)
- (Dropout added in CustomCNN to prevent overfitting)

Fully Connected Layers:
- LeNet: 16x4x4 → 120 → 84 → 10
- CustomCNN: 64x14x14 → 128 → 10
- (Simplified and regularized fully connected layers in CustomCNN)

Regularization:
- LeNet: None
- CustomCNN: Dropout regularization

Total Parameters:
- LeNet: Lower
- CustomCNN: Slightly higher
- (CustomCNN is more expressive and powerful)

Expected Accuracy:
- LeNet: ~98%
- CustomCNN: ~98.5% to 99%
- (CustomCNN is expected to perform slightly better)