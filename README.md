# Plant Disease Classification Using Convolutional Neural Networks
---

## Objectives

- To develop an **automated image classification model** capable of detecting plant diseases in potato leaves.  
- To evaluate the **performance of CNN-based deep learning models** for agricultural image recognition tasks.  
- To improve model robustness using **data augmentation and preprocessing techniques**.  
- To demonstrate the potential of **AI-driven tools** in the field of **smart agriculture**.

---

## Dataset Description

The model utilizes the **PlantVillage Dataset**, a publicly available benchmark dataset for plant disease classification tasks.  
For this project, only the **Potato Leaf Subset** is used, containing images categorized as:

| Class Label | Description |
|--------------|-------------|
| Potato___Early_Blight | Leaves affected by the Early Blight fungal disease |
| Potato___Late_Blight | Leaves affected by the Late Blight fungal disease |
| Potato___Healthy | Healthy potato leaves without visible disease symptoms |

**Dataset Source:** [PlantVillage Dataset (Kaggle)](https://www.kaggle.com/datasets/arjuntejaswi/plant-village)

**Data Preprocessing Steps:**
- Image resizing to **256 × 256 pixels**
- Application of data augmentation (rotation, horizontal/vertical flip)

---

## Model Architecture

The proposed model is based on a **Sequential CNN architecture** developed using **TensorFlow and Keras**.  
The architecture includes:

1. **Input Layer**  
   - Image input size: `256×256×3`  
   - Rescaling and normalization  

2. **Data Augmentation Block**  
   - Random rotations, flips, and zooms to prevent overfitting  

3. **Convolutional Layers**  
   - Multiple convolutional blocks using `Conv2D` with ReLU activation  

4. **Pooling Layers**  
   - `MaxPooling2D` layers for dimensionality reduction  

5. **Flatten Layer**  
   - Converts feature maps into a 1D vector  

6. **Fully Connected (Dense) Layers**  
   - Hidden layers with ReLU activation for feature learning  

7. **Output Layer**  
   - `Dense` layer with `softmax` activation (3 output classes)  

---

## ⚙️ Model Training Configuration

| Parameter | Value |
|------------|--------|
| Optimizer | Adam |
| Loss Function | Sparse Categorical Crossentropy |
| Epochs | 40 |
| Batch Size | 32 |
| Evaluation Metric | Accuracy |

**Training Strategy:**
- The dataset is split into training, validation, and test sets.  
- The model is trained for 40 epochs with real-time data augmentation.  
- Performance is monitored using accuracy and loss curves.

---

## Model Evaluation

Model evaluation is performed using unseen test data to assess generalization ability.
Visualization tools such as **Matplotlib** are used to plot accuracy and loss trends over training epochs.

## Dependencies
- pandas
- numpy
- matplotlib
- tensorflow
