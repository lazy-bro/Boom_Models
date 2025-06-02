This project implements a Convolutional Neural Network (CNN) using Keras to classify images from the CIFAR-10 dataset, achieving an accuracy of 83% on the test set.

🔍 Dataset
The CIFAR-10 dataset consists of 60,000 32x32 color images in 10 different classes:
Airplane
Automobile
Bird
Cat
Deer
Dog
Frog
Horse
Ship
Truck
🏗️ Model Architecture
The CNN architecture is designed with:

Convolutional layers with ReLU activation and same padding

Batch Normalization to stabilize learning

MaxPooling for downsampling

Dropout layers to reduce overfitting

A fully connected dense layer with 512 units

Output layer with softmax activation (10 classes)

🔧 Data Augmentation
Applied real-time data augmentation using ImageDataGenerator:

Rotation: 15°

Width and height shift: 10%

Horizontal flip

Zoom range: 10%

🧪 Training Details
Optimizer: Adam
Loss Function: Sparse Categorical Crossentropy
Batch Size: 64
Epochs: Up to 100 (early stopping can be added)
Validation: 20% test split from CIFAR-10

📈 Results
Achieved ~83% test accuracy
Trained and evaluated using TensorFlow/Keras

🛠️ Future Improvements
Implement learning rate scheduling
Try other architectures (e.g., ResNet, VGG)
Add model checkpointing and improved callbacks
