# Practicing transfer learning

## Introduction

This file is a step by step tutorial to practice basics of transfer learning on
an industrial dataset composed of pictures, for a use case of quality control.
You will also find the dataset and Jupyter notebooks with code that could help
you address the questions.

## Cast defect dataset

- available in `casting_512x512.zip` or on Kaggle: <https://www.kaggle.com/datasets/ravirajsinh45/real-life-industrial-dataset-of-casting-product>
- This dataset provides image data of impellers for submersible pumps.
- There are many types of defect in casting like blow holes, pinholes, burr,
shrinkage defects, mould material defects, pouring metal defects, metallurgical
defects, etc.
- Raw dataset = 519 ok + 781 defect
- (Kaggle also has an already augmented dataset = 7348 pictures)

## Carry out transfer learning with a pretrained DL image classification model

- Use this Keras tutorial:
- <https://keras.io/guides/transfer_learning/>
- Take a pretrained DL image classification model
- Freeze weights
- Remove last layer
- Replace it by what makes sense to your question
- Train only the part you added
- See `defects_transfer.ipynb` for example code

## What tweaks to try

- With different kinds of image classification models
- With different layers on top of the pre-trained model
- With or without data augmentation
- With a different number of input pictures

Possible output:
|Scenario|Type-of-model|Data-augmentation|Number-of-training-images|Number-of-test-images|Training-accuracy|Testing-accuracy|Training-duration|
|-|-|-|-|-|-|-|-|
|1..n|Xception,MobileNet,ResNet,...|y/n|5%-10%-50%-80%-of-total|||||

## Ideas to go further

- Explainability

## Classic CV approach (optional)

- SIFT (or AKAZE)
- Bag of words
- Classification with SVM
- See `defects_AKAZE_SVM.ipynb`
