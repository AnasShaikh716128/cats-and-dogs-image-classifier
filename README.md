# Cats and Dogs Image Classifier

This project contains a Jupyter Notebook that builds and trains a Convolutional Neural Network (CNN) to classify images of cats and dogs.

## Overview

The notebook demonstrates:

- Loading and exploring the dataset
- Preparing image data using `ImageDataGenerator`
- Augmenting images to improve generalization
- Building a CNN model with TensorFlow/Keras
- Training and validating the model
- Plotting training metrics
- Evaluating model accuracy against a challenge dataset

## Project Files

- `cats_and_dogs.ipynb` — main training and evaluation notebook
- `README.md` — project documentation

## Requirements

To run the notebook, install the following Python packages:

```bash
pip install tensorflow matplotlib scipy pandas notebook
```

Recommended:

- Python 3.10+
- TensorFlow 2.x
- Jupyter Notebook or JupyterLab

## Dataset

The notebook expects a dataset named:

```text
cats_and_dogs.zip
```

After extraction, it uses a folder structure like this:

```text
cats_and_dogs/
├── train/
│   ├── cats/
│   └── dogs/
├── validation/
│   ├── cats/
│   └── dogs/
├── test/
```

The dataset is processed using Keras `flow_from_directory`, which reads images directly from the folder structure.

## Notebook Workflow

The notebook performs the following steps:

1. Extract the dataset zip file.
2. Define image paths and dataset directories.
3. Create training, validation, and test generators.
4. Resize images to `150x150`.
5. Apply rescaling and augmentation.
6. Build a CNN model with convolutional and pooling layers.
7. Compile the model with binary cross-entropy loss.
8. Train the model for 15 epochs.
9. Visualize accuracy and loss trends.
10. Evaluate the model on test images and compare predictions to expected answers.

## Model Architecture

The CNN includes:

- `Conv2D` layers
- `MaxPooling2D` layers
- `Flatten`
- `Dense` layers
- `Dropout` (included in the imported layers, although not heavily used in the final model)
- Final sigmoid output for binary classification

## Run the Notebook

Open the notebook in Jupyter:

```bash
jupyter notebook cats_and_dogs.ipynb
```

Then run all cells sequentially.

## Notes

- The notebook prints the model's classification accuracy percentage.
- It checks whether the model passes a challenge threshold of 63% correct predictions.
- The project is intended as a beginner-friendly deep learning example for image classification.

## License

This project does not include a specific license file in the provided notebook context. If this is being used publicly, you may want to add an appropriate license such as MIT or Apache 2.0.

## Author

Built as a TensorFlow/Keras image classification project for identifying cats and dogs from image data.
