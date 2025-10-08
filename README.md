# Plant Disease Classification Using Deep Learning
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
