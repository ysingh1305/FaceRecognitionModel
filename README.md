# Siamese Face Recognition Model

This project implements a **Siamese Neural Network** for face recognition using TensorFlow and Keras. The model is designed to learn meaningful representations of facial images and determine whether two input images represent the same person.

## Project Highlights

- Developed a custom embedding model using Convolutional Neural Networks (CNNs)
- Used cv2 and TensorFlow pipelines to efficiently load, resize, and normalize image data for model training
- Used a **Siamese Network** architecture with a custom **L1 Distance Layer**
- Achieved effective training using binary cross-entropy and the Adam optimizer
- Includes metrics for **Precision** and **Recall** to evaluate model performance

## How It Works

1. **Data Preprocessing**  
   Images are resized to 100x100 and normalized between 0 and 1.

2. **Embedding Model**  
   A CNN-based architecture is used to map input images to a high-dimensional vector space.

3. **Siamese Network**  
   - Takes an anchor and a test image (positive or negative).
   - Calculates the **L1 distance** between their embeddings.
   - Outputs a similarity score using a sigmoid-activated Dense layer.

4. **Training**  
   The model is trained using binary labels (1 = same person, 0 = different) and optimized using binary cross-entropy.

5. **Evaluation**  
   After training, the model evaluates precision and recall on test pairs.
