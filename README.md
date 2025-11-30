# INTEL_IMAGE_CLASSIFICATION

This project is about classifying images into 6 different categories. The dataset can be downloaded from Kaggle.

## Model Details

- **Model Used**: VGG16
  - Imported from Keras.
  - Removed the top layer.
  - Made the last convolution block (5th block) parameters trainable.
  - Used the same weights for layers 1 to 4 as when pretrained on the ImageNet dataset.

- **Training Details**:
  - Trained on augmented data from the Intel Images dataset.
  - Applied dropout layers and used early stopping with patience=5.
  - Achieved 93% accuracy on training data and 89% accuracy on test data.
  - Training was performed over 22 epochs with 329 steps each.

- **Evaluation**:
  - Used Matplotlib to plot:
    - Training and validation accuracy
    - Training and validation loss
  - The plots show similar behavior for training and validation metrics.

- **Model Saving**:
  - Saved the trained model using Keras utility: `model.save('model.h5')`.

## Repository Structure

- **Notebooks**:
  1. **Intel_Image_Classification**: Demonstrates how the model was trained and performance was visualized.
  2. **Classify_Images**: Loads the saved model and classifies images.

- **Directory**:
  - **test_the_input**: Contains test images for evaluating the model.

## Model Download

The model can be downloaded from my Google Drive link: [Download model.h5](https://drive.google.com/file/d/130OPjHVOfB2ERjJP0DOu9xCHlB5tnxT8/view?usp=drive_link)
