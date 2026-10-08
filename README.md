# 5×5 Image Anomaly Detection

## Project Overview

This project detects anomalies in a **5×5 grayscale image** using image processing, convolution, ReLU activation, feature extraction, and machine learning.

The main objective is to identify whether an input image or extracted feature pattern is **Normal** or **Anomalous**.

---

## Project Method

The overall processing pipeline is:

```text
5×5 Grayscale Image
        ↓
3×3 Filter
        ↓
Convolution
        ↓
ReLU Activation
        ↓
Feature Extraction
        ↓
Isolation Forest
        ↓
Normal / Anomaly
Input Image

The input is a 5×5 grayscale image represented as a matrix of pixel values.

Example:

[ 10  12  11  10  13 ]
[ 11  10  12  11  10 ]
[ 12  11  10  12  11 ]
[ 10  13  12  11  10 ]
[ 11  10  11  12  13 ]

Each value represents the intensity of a pixel.

Convolution

A 3×3 filter is applied to the 5×5 input image.

The filter moves across the image and performs element-wise multiplication followed by summation.

The convolution operation extracts important local features from the image.

The output size depends on the input size, filter size, padding, and stride.

For a 5×5 input with a 3×3 filter, stride = 1, and no padding, the output feature map is:

(5 - 3) / 1 + 1 = 3

Therefore, the convolution produces a:

3×3 feature map
ReLU Activation

After convolution, the ReLU activation function is applied.

The ReLU function is:

ReLU(x) = max(0, x)

This means:

Negative values become 0.
Positive values remain unchanged.

Example:

Before ReLU:

[-2   4  -1]
[ 3  -5   6]
[-1   2   0]

After ReLU:

[0   4   0]
[3   0   6]
[0   2   0]

ReLU introduces non-linearity and helps the model learn useful patterns.

Feature Extraction

The ReLU output is treated as the extracted feature representation.

These features contain information about the patterns present in the image.

The extracted features are then provided to the anomaly detection model.

Anomaly Detection

The project uses the Isolation Forest algorithm for anomaly detection.

Isolation Forest is an unsupervised machine learning algorithm that identifies unusual observations by isolating them from normal observations.

The output is classified into:

Normal

or

Anomaly

An image or feature vector that differs significantly from the learned normal patterns can be identified as an anomaly.

Technologies Used
Python
NumPy
Matplotlib
Scikit-learn
Google Colab
Jupyter Notebook
GitHub
Libraries Used
NumPy

Used for:

Matrix operations
Image representation
Numerical calculations
Convolution calculations
Matplotlib

Used for:

Displaying images
Plotting matrices
Visualizing results
Scikit-learn

Used for:

Isolation Forest
Machine learning-based anomaly detection
Model evaluation
Mathematical Process

The project follows these main mathematical steps:

1. Convolution

A 3×3 filter is applied to the 5×5 input image.

For each position:

Convolution Output =
Sum(Input Region × Filter)
2. ReLU

The convolution output is passed through:

ReLU(x) = max(0, x)
3. Feature Extraction

The resulting feature values are used as the feature representation of the image.

4. Isolation Forest

The extracted features are analyzed to determine whether the sample follows the normal pattern or is significantly different.

Example Processing
Input:

5×5 Image
    ↓
3×3 Filter
    ↓
Convolution
    ↓
3×3 Feature Map
    ↓
ReLU
    ↓
Non-negative Features
    ↓
Feature Vector
    ↓
Isolation Forest
    ↓
Normal / Anomaly
Objective

The main objectives of this project are:

Represent a grayscale image as a matrix.
Apply a 3×3 convolution filter.
Understand feature extraction using convolution.
Apply ReLU activation.
Extract useful features.
Apply Isolation Forest for anomaly detection.
Classify the input as Normal or Anomaly.
Understand the mathematical operations involved in CNN-based image processing.
Results

The model produces an anomaly detection result for the input feature pattern.

The final output is:

Normal

or

Anomaly

The exact result depends on the input image, filter values, extracted features, and Isolation Forest model.

Project Structure
5x5-image-anomaly-detection/
│
├── 5x5_Image_Anomaly_Detection.ipynb
├── README.md
└── .gitignore
How to Run
Open the Jupyter Notebook in Google Colab.
Run the cells sequentially.
Enter or generate the 5×5 grayscale image.
Apply the 3×3 convolution filter.
Calculate the feature map.
Apply ReLU activation.
Extract the features.
Apply Isolation Forest.
Observe the final Normal/Anomaly prediction.
Conclusion

This project demonstrates how basic image processing and machine learning techniques can be combined for anomaly detection.

A 5×5 grayscale image is processed using a 3×3 convolution filter to extract local features. The ReLU activation function removes negative feature values and introduces non-linearity.

The extracted features are then analyzed using Isolation Forest to determine whether the input pattern is normal or anomalous.

The project provides a simple demonstration of the relationship between:

Image → Convolution → ReLU → Feature Extraction → Anomaly Detection
