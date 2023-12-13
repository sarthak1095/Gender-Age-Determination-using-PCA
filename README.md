# Gender-Age-Determination-using-PCA

### Project Overview

This study explores Gender and Age Determination, utilizing the UTK Faces Dataset. In this framework, the study explored the effectiveness of PCA for
dimensionality reduction and feature extraction. The outcome was a multi-output concurrent neural network capable of simultaneously predicting gender and age for test images. In conclusion,
the study found that dimensionality reduction with PCA retained a significant amount of essential information in the data. Gender classification achieved a remarkable accuracy rate,
effectively distinguishing between male and female individuals. The age regression model exhibited good accuracy with a mean absolute error MAE measure, although challenges remained in estimating ages for very young and old individuals.

### Aim
- To develop models for gender classification and age regression using deep learning techniques on the UTK Faces dataset.

Objective
- Explored the utility of PCA for dimensionality reduction and feature extraction.
- Created a multi-output concurrent neural network that simultaneously predicted gender and age for test images with high precision.

### Pipeline

The process began with the importation of the necessary libraries. Subsequently, data exploration was undertaken to gain insights into the dataset, including its structure and characteristics.
Data preprocessing followed, involving the encoding of categorical variables and the division of the data into training and testing sets. Feature extraction was performed to identify and select
relevant features from the dataset, and PCA was applied to reduce dimensionality. A concurrent gender and age model was implemented, and this model was trained using the PCAtransformed
data. After training, the model's performance was evaluated using appropriate metrics. Once the model's performance was estimated efficient, predictions were generated
using new data. Finally, results were visualized to provide a clear understanding of the model's performance and predictions. This sequence of steps outlines a typical workflow for a concurrent gender and age prediction task, where the model was trained using PCA transformed data.

### Model Architecture

The architecture outlines the creation of a neural network model using the Keras functional API. This model was designed for gender classification and age regression tasks. It consists
of several dense layers with ReLU activation and batch normalization for both tasks. 17 Dropout layers were added after each batch normalization layer to mitigate overfitting. The
model's gender classification branch includes three dense layers and a sigmoid-activated output layer for binary classification. The age regression branch also comprises three dense layers,
ending in a rectified linear unit (ReLU) activated output layer. The model uses binary crossentropy loss for gender classification and mean absolute error loss for age regression. The Adam
optimizer was used, and accuracy was monitored. The resulting multi-output network performs simultaneous gender classification and age regression. The model summary provides
architecture and layer details (Figure 16). Training used 30 epochs, batch size 64, and 25% validation split. Learning rate scheduling and early stopping were callback implementations.
Training and validation accuracy for gender classification were recorded. Graphs visualize training and validation accuracy and loss for gender classification and age regression, providing performance overview.

### Evaluation

In the process of evaluation, the model's performance on the test set, several key metrics were examined, including overall loss, gender loss, age loss, gender accuracy, and age MAE on its
effectiveness in gender classification and age regression.

Gender Loss: The model's gender loss, measured through binary cross-entropy, was 0.3628. This figure represents the average loss incurred during the gender classification process. Lower
values indicate superior performance, signifying that the model's gender predictions closely align with the true gender labels.

Gender Accuracy: Achieving an impressive accuracy rate of 88.19%, the model correctly predicts gender labels for a significant portion of the test samples. A higher accuracy score indicates
the model's proficiency in distinguishing between male and female individuals within the dataset.

Age MAE: The age MAE serves as a measure of the absolute difference between the model's age predictions and the actual age values. In this instance, the age MAE stands at 0.01. This
small MAE suggests that, on average, the model's age predictions closely approximate the true ages of individuals in the dataset. These insights collectively affirm the model's competence in both gender classification and age regression tasks, showcasing its accuracy and precision in these critical aspects of the analysis.
