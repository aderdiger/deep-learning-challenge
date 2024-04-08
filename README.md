# Analysis of Deep Learning Model Optimization and Performance

### Overview of the Analysis:
The purpose of this analysis is to develop a deep learning model using neural networks to predict the success of applicants from Alphabet Soup. The model aims to classify whether an applicant will be successful if funded based on various features provided in the dataset.

### Results:

#### Data Preprocessing:

- **Target Variable:**
  - The target variable for the model is the "IS_SUCCESSFUL" column, indicating whether an applicant was successful if funded.

- **Features:**
  - Features include various columns such as "APPLICATION_TYPE," "AFFILIATION," "CLASSIFICATION," etc., providing information about the applicants.
  - Despite "NAME" not directly contributing to prediction, it was retained in the input data due to its impact on accuracy.
    
- **Variables to be Removed:**
  - "EIN" is a unique identifiers and does not contribute to the prediction. Therefore, it was removed from the input data.

#### Compiling, Training, and Evaluating the Model:

- **Neurons, Layers, and Activation Functions:**
  - Two hidden layers with 7 neurons each were selected to balance complexity and performance.
  - ReLU activation functions were chosen for all hidden layers to introduce non-linearity.
  - The output layer used a sigmoid activation function for binary classification.

- **Model Performance:**
  - The model achieved an accuracy of approximately 79%, exceeding the target accuracy of 75%.
  - The loss value was approximately 0.55, indicating moderate performance.


### Steps Taken to Increase Model Performance:

#### Attempt #1:
- **Architecture**:
  - Two hidden layers with 5 neurons each.
- **Performance**:
  - Loss: 0.593
  - Accuracy: 0.775
- **Observation**:
  - Initial attempt with a simple architecture achieved decent accuracy but relatively high loss.

#### Attempt #2:
- **Architecture**:
  - Three hidden layers with 7 neurons each.
- **Performance**:
  - Loss: 0.536
  - Accuracy: 0.764
- **Observation**:
  - Increased complexity by adding an extra layer and more neurons.
  - However, the test accuracy decreased despite the increase in parameters, suggesting potential overfitting.

#### Attempt #3:
- **Architecture**:
  - Two hidden layers with 7 neurons each.
- **Changes**:
  - Increased the number of epochs to 200.
- **Performance**:
  - Loss: 0.551
  - Accuracy: 0.787
- **Observation**:
  - Simplified the architecture back to two hidden layers.
  - Increased the number of epochs to 200, leading to a slight improvement in accuracy compared to Attempt #1.

### Summary:

The deep learning model successfully surpassed the target accuracy of 75%, achieving approximately 79% accuracy. Despite "NAME" not directly contributing to prediction, its retention in the input data improved model accuracy.

Each attempt involved adjusting the architecture or hyperparameters to optimize model performance. While Attempt #2 introduced additional complexity, it did not improve accuracy and potentially led to overfitting. Attempt #3, on the other hand, simplified the architecture and focused on fine-tuning epochs, resulting in a slight improvement in accuracy compared to the initial attempt. This iterative process of experimentation and refinement is crucial for developing effective deep learning models. 

Further improvements could involve fine-tuning hyperparameters or exploring more advanced architectures to potentially increase accuracy while ensuring generalization to unseen data.

Given the model's current performance and feature selection strategy, it provides a solid foundation for predicting applicant success, meeting the specified target accuracy, and aiding decision-making processes at Alphabet Soup. Continued refinement and experimentation may lead to even better predictive capabilities in the future.
