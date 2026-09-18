# PlantDoc – Plant Disease Classification

## Project Overview

Plant diseases can significantly affect crop quality and agricultural productivity. Early identification of plant diseases can help farmers take appropriate action before diseases spread and cause greater losses.

This project develops a deep learning image classification system using the **PlantDoc dataset** to identify plant diseases from leaf images. The project explores image preprocessing, data augmentation, convolutional neural networks, transfer learning, model evaluation, and model interpretability.

The final approach uses **MobileNetV2 transfer learning** to classify plant leaf images into multiple plant disease categories.

## Business Context

In agriculture, identifying plant diseases manually can be time-consuming and may require expert knowledge. An image-based classification system can provide a supporting tool for faster identification of visible plant diseases.

The proposed system demonstrates how deep learning can be applied to agricultural image data to support early plant disease detection.

## Project Question

**How effectively can a deep learning image classification model identify plant diseases from plant leaf images?**

## Dataset

The project uses the publicly available **PlantDoc dataset**.

The dataset contains plant images representing different plant species and disease categories. The classification task contains **27 classes**.

The dataset was obtained from Kaggle and is downloaded within the notebook.

## Machine Learning Problem

This project is formulated as a:

**Multi-class image classification problem**

### Input

RGB image of a plant leaf.

### Output

One of 27 plant species/disease classes.

## Methodology

The project follows an end-to-end deep learning workflow:

1. Dataset loading
2. Dataset exploration
3. Data quality inspection
4. Image preprocessing
5. Image augmentation
6. Model development
7. Model experimentation
8. Model validation
9. Final model selection
10. Testing on unseen images
11. Grad-CAM interpretability
12. Discussion and recommendations

## Model

The final model uses **MobileNetV2** with transfer learning.

MobileNetV2 was selected because it provides a lightweight convolutional neural network architecture that can learn useful visual features while requiring fewer computational resources than many larger deep learning architectures.

The model was adapted for the PlantDoc multi-class classification task.

## Evaluation

Model performance was evaluated using validation and test data.

The evaluation considers the model's ability to correctly classify plant disease images and examines its behaviour on previously unseen images.

The notebook also includes visual analysis of model predictions and **Grad-CAM** visualisations to investigate which image regions contributed to model predictions.

## Interpretability

**Grad-CAM (Gradient-weighted Class Activation Mapping)** is used to provide visual explanations of the model's predictions.

This helps examine whether the model is focusing on relevant regions of plant leaf images when making its classification decisions.

## Key Findings

The project demonstrates that transfer learning with MobileNetV2 can learn useful visual patterns from plant images for multi-class disease classification.

The analysis also highlights the importance of:

* Image quality
* Dataset size
* Class balance
* Image preprocessing
* Data augmentation
* Validation on unseen data
* Model interpretability

Further external validation would be required before considering the system for real-world agricultural deployment.

## Technologies Used

* Python
* TensorFlow
* Keras
* MobileNetV2
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* Jupyter Notebook
* Grad-CAM

## Repository Structure

```text
PlantDoc-Plant-Disease-Classification/
│
├── README.md
└── MOP_FINAL.html
```

## Notebook

The complete project analysis and implementation are available in:

**`MOP_FINAL.html`**

The notebook contains the complete workflow from dataset loading and exploration through model development, evaluation, and interpretation.

## Limitations

The project has several limitations:

* The dataset may not represent all real-world agricultural conditions.
* Images captured in controlled or different environments may differ from field images.
* Class distribution and image quality can affect model performance.
* Further testing with independent real-world datasets would be required.
* The model should be considered a research/academic prototype rather than a production agricultural diagnostic system.

## Future Improvements

Potential improvements include:

* Training with larger and more diverse agricultural datasets.
* Testing additional transfer-learning architectures.
* Improving class balance.
* Performing more extensive hyperparameter optimisation.
* Testing the model on real-world field images.
* Developing a simple web or mobile application for image-based predictions.
* Further improving model interpretability.

## References

* Singh et al. (2020). PlantDoc: A Dataset for Visual Plant Disease Detection.
* Selvaraju et al. (2017). Grad-CAM: Visual Explanations from Deep Networks via Gradient-based Localization.
* TensorFlow and Keras documentation.
* Kaggle PlantDoc Dataset.
