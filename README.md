# Scene Image Classification (CNN)

Convolutional neural network that classifies natural scene images into 6 classes: buildings, forest, glacier, mountain, sea, and street.

## Dataset
[Intel Image Classification](https://www.kaggle.com/datasets/puneet6060/intel-image-classification): 14,034 training and 3,000 validation images, resized to 150x150.

## Model
- Sequential CNN: 4 x (Conv2D + MaxPooling2D), Flatten, Dropout (0.5), Dense (512), softmax (6)
- Augmentation: rotation, horizontal flip, shear, zoom
- Optimizer: Adam (lr 0.001), loss: categorical crossentropy, 50 epochs

## Results
| Metric | Value |
|---|---|
| Training accuracy | 91.8% |
| Validation accuracy | 83.6% (peak 87.8%) |

## Exported Formats
- `saved_model/`: TensorFlow SavedModel
- `tflite/`: TF-Lite model and `label.txt`
- `tfjs_model/`: TensorFlow.js model

## Run
1. `pip install -r requirements.txt`
2. Open `notebook.ipynb` (written for Google Colab; Kaggle API credentials are needed to download the dataset).

## Author
R. Haikal Rizki Tri Hartanto, [github.com/haikalrth](https://github.com/haikalrth)
