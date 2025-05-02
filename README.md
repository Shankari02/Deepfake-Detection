# Deepfake-Detection
A deep learning-based system for detecting deepfake images using Convolutional Neural Networks (CNN) and U-Net, aimed at improving digital media authenticity.

# 🔍 Deepfake Image Detection using Deep Learning

## 🧾 Introduction

With the growing sophistication of AI-generated content, detecting deepfake images has become critical for preserving digital authenticity. This project focuses on identifying manipulated facial images using deep learning models.

## 📌 Project Overview

We implemented and compared various deep learning architectures to classify images as real or fake. The dataset, obtained from Kaggle, consists of labeled facial images. Our goal was to build a model pipeline that can reliably detect deepfakes with high accuracy and generalization.

The project includes:
- Image preprocessing and augmentation
- Implementation of multiple models
- Visualization of training metrics
- Performance comparison

## 🧠 Models Implemented

| Model                | Description |
|---------------------|-------------|
| **Custom CNN**       | A baseline convolutional neural network created from scratch to establish reference performance. |
| **U-Net (Normal)**   | Standard U-Net architecture adapted for image classification, traditionally used in segmentation. |
| **U-Net (Improvised)** | Enhanced U-Net with deeper layers, batch normalization, and dropout to improve accuracy. |
| **DenseNet**         | Utilizes dense connections between layers to improve gradient flow and feature reuse. |
| **EfficientNet**     | Balances model depth, width, and resolution for optimal performance with fewer parameters. |
| **ResNet**           | Deep residual network with skip connections to address vanishing gradients in deep networks. |

## 🧹 Preprocessing of Dataset

### 📂 Splitting and Restructuring

- **Image Resizing**: All images were resized to a fixed dimension (e.g., 128×128 or 256×256).
- **Normalization**: Pixel values scaled to [0, 1] to improve model convergence.
- **Dataset Split**:
  - 70% Training
  - 15% Validation
  - 15% Test
- **Label Encoding**: Categorical labels encoded as 0 (real) and 1 (fake).
- **Shuffling**: Ensured randomness during training.
- **Data Augmentation**: Included horizontal/vertical flips, brightness and rotation variations to improve generalization.

## 📈 Performance

Training and validation accuracy/loss were tracked over multiple epochs. Below are the observations:

- All models successfully learned to distinguish deepfakes from real images.
- **Improvised U-Net**, **EfficientNet**, and **ResNet** outperformed others in validation accuracy.
- Accuracy/loss plots indicate stable training with minimal overfitting in well-regularized models.

📊 *Example insight*: The **Improvised U-Net** achieved a **testing accuracy of 72.22%**, showing strong generalization capabilities and effective deepfake detection performance.

## ✅ Conclusion

This project successfully demonstrates the application of deep learning techniques for detecting deepfake images. Among the implemented models, the Improvised U-Net achieved the best balance between performance and complexity with a testing accuracy of **72.22%**. The project highlights the importance of model architecture, preprocessing, and augmentation in improving detection accuracy.

## 🔮 Future Enhancements

- **Model Optimization**: Further tuning of hyperparameters and use of learning rate schedulers.
- **Larger Dataset Integration**: Incorporating larger and more diverse datasets to improve robustness.
- **Multi-modal Deepfake Detection**: Extend to video and audio-based deepfake detection systems.
- **Explainability**: Add Grad-CAM or saliency maps to visualize which features influence predictions.
- **Deployment**: Package the best-performing model into a web or mobile application for real-time usage.

## 👥 Contributors

- Yash Jain
- Reegan Pinto
- Anoushka Ruikar
- Shankari Anandakrishnan    
- Aditya Vivekanand  

