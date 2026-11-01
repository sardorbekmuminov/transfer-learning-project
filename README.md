# Image Classification with Transfer Learning

## Project Overview

This project explores image classification using the **ResNet18** convolutional neural network and the **ImageWoof160** dataset.

The main objective is to compare different training strategies and understand how transfer learning can improve image classification performance.

Three approaches are implemented:

* Training from scratch
* Feature extraction
* Fine-tuning

The project was developed using Python and PyTorch in a Jupyter Notebook environment.

## Objectives

* Understand the fundamentals of transfer learning.
* Compare training a neural network from scratch with pretrained model approaches.
* Explore feature extraction using a pretrained CNN.
* Apply fine-tuning to adapt a pretrained model to a new task.
* Evaluate and compare model accuracy.

## Dataset

The project uses the **ImageWoof160** dataset, a subset of ImageWoof containing images from 10 dog breeds.

The dataset is downloaded automatically in the notebook.

The model is trained to classify images into the following categories:

* Shih-Tzu
* Ridgeback
* Beagle
* Foxhound
* Border Terrier
* Aussie Terrier
* Golden Retriever
* Sheepdog
* Samoyed
* Dingo

Images are resized to 128 × 128 pixels and normalized using the ImageNet mean and standard deviation.

## Methods

### 1. Training from Scratch

A ResNet18 model is initialized without pretrained weights and trained on the target dataset.

This approach provides a baseline for understanding how a model learns when it does not use previously learned features.

### 2. Feature Extraction

A pretrained ResNet18 model is used as a feature extractor.

The pretrained backbone generates image features, and a new fully connected classification layer is trained to classify the 10 target classes.

This approach takes advantage of features learned from a larger dataset while keeping the backbone fixed.

### 3. Fine-tuning

A pretrained ResNet18 model is adapted to the ImageWoof160 dataset.

The final classification layer is adjusted for the 10 target classes, and the model parameters are trained to improve performance on the target task.

## Results

The notebook produced the following accuracy results:

| Method                | Accuracy |
| --------------------- | -------: |
| Training from Scratch |      28% |
| Feature Extraction    |    82.3% |
| Fine-tuning           |      80% |

The results show that pretrained models performed substantially better than training ResNet18 from scratch in this experiment.

Feature extraction achieved the highest reported accuracy among the three approaches.

*Note: These values represent the results recorded in the notebook. Performance may vary depending on the training configuration and environment.*

## Technologies Used

* Python
* PyTorch
* timm
* NumPy
* PIL (Pillow)
* Matplotlib
* Jupyter Notebook

## Project Structure

```text
transfer-learning-project/
├── README.md
└── transfer_learning.ipynb
```

## How to Run

1. Open `transfer_learning.ipynb` in Google Colab or Jupyter Notebook.
2. Make sure the required libraries are installed.
3. Run the notebook cells from top to bottom.
4. The notebook downloads and prepares the dataset.
5. Review the training process, accuracy results, and predictions.

## Model Saving

The fine-tuned model's parameters are saved in a file named:

```text
model.pt
```

The notebook also demonstrates how to make predictions and visualize an example image.

## Conclusion

This project demonstrates the practical application of transfer learning for image classification.

By comparing training from scratch, feature extraction, and fine-tuning, the experiment illustrates how pretrained models can provide useful features for a new classification task.

The results show that using a pretrained ResNet18 can substantially improve classification accuracy compared with training the model from scratch.

This project provided practical experience with convolutional neural networks, model training, feature extraction, fine-tuning, and image classification using PyTorch.
