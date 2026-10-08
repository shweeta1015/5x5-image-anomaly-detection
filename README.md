# 5×5 Image Anomaly Detection

## Abstract

This project presents an image anomaly detection approach using a 5×5 grayscale image, convolution-based feature extraction, ReLU activation, and the Isolation Forest machine learning algorithm.

The objective is to demonstrate how low-level image processing techniques can be combined with an unsupervised machine learning algorithm to identify abnormal patterns in image data.

---

## Objectives

The primary objectives of this project are:

- To represent a grayscale image as a numerical matrix.
- To perform convolution using a 3×3 filter.
- To extract meaningful features from the input image.
- To apply the ReLU activation function.
- To analyze the extracted features using Isolation Forest.
- To classify the input pattern as normal or anomalous.
- To demonstrate the mathematical operations involved in image-based anomaly detection.

---

## Methodology

The proposed methodology consists of the following stages:

```text
5×5 Grayscale Image
        ↓
3×3 Convolution Filter
        ↓
Convolution Operation
        ↓
ReLU Activation
        ↓
Feature Extraction
        ↓
Isolation Forest
        ↓
Normal / Anomaly
Input Data

The input is represented as a 5×5 grayscale image matrix. Each element of the matrix represents the intensity value of a pixel.

A grayscale image contains a single channel, where the pixel intensity represents the brightness of the corresponding pixel.

Convolution Operation

A 3×3 convolution filter is applied to the 5×5 input image.

For each position of the filter, element-wise multiplication is performed between the filter and the corresponding image region, followed by summation.

The convolution operation can be represented as:

Convolution Output = Σ(Input Region × Filter)

For a 5×5 input, a 3×3 filter, stride = 1, and no padding, the output feature map size is:

Output Size = (Input Size - Filter Size) / Stride + 1

Output Size = (5 - 3) / 1 + 1

Output Size = 3

Therefore, the resulting feature map has dimensions:

3 × 3
ReLU Activation

The Rectified Linear Unit (ReLU) activation function is applied to the convolution output.

The mathematical representation of ReLU is:

ReLU(x) = max(0, x)

The function converts negative values to zero while retaining positive values.

ReLU introduces non-linearity into the feature representation and enables the model to learn more complex patterns.

Feature Extraction

The output obtained after applying ReLU represents the extracted feature map.

These features provide information about local patterns and structures present in the input image.

The extracted feature values are subsequently converted into a suitable representation for anomaly detection.

Anomaly Detection Using Isolation Forest

The extracted features are analyzed using the Isolation Forest algorithm.

Isolation Forest is an unsupervised machine learning algorithm designed to identify anomalous observations.

The algorithm works by isolating observations through recursive partitioning. Anomalous observations generally require fewer partitions to become isolated because they differ significantly from the majority of the data.

The final prediction categorizes the input as:

Normal
Anomaly
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

NumPy is used for numerical computations, matrix representation, and convolution-related operations.

Matplotlib

Matplotlib is used for image visualization and graphical representation of results.

Scikit-learn

Scikit-learn is used to implement the Isolation Forest anomaly detection algorithm.

Mathematical Workflow

The mathematical processing can be summarized as follows:

Step 1: Input Representation

The 5×5 grayscale image is represented as a matrix:

I ∈ R⁵ˣ⁵
Step 2: Convolution

A 3×3 filter is applied to the image:

F ∈ R³ˣ³

The convolution produces a 3×3 feature map.

Step 3: ReLU

The convolution output is transformed using:

R(x) = max(0, x)
Step 4: Feature Representation

The resulting feature map is converted into a feature vector for anomaly detection.

Step 5: Anomaly Detection

The feature vector is provided to the Isolation Forest model to determine whether the sample represents a normal or anomalous pattern.

Experimental Workflow

The complete implementation follows these steps:

Define the 5×5 grayscale input image.
Define a 3×3 convolution filter.
Perform the convolution operation.
Generate the feature map.
Apply the ReLU activation function.
Extract the resulting features.
Train or apply the Isolation Forest model.
Generate the anomaly prediction.
Visualize the intermediate and final results.
Results

The system generates an anomaly classification based on the extracted image features.

The final classification is represented as:

Normal

or

Anomaly

The result depends on the input image, convolution filter, extracted feature representation, and Isolation Forest configuration used in the experiment.

Project Structure
5x5-image-anomaly-detection/
│
├── 5x5_Image_Anomaly_Detection.ipynb
├── README.md
└── .gitignore
How to Run the Project
Open the Jupyter Notebook in Google Colab.
Run the cells sequentially.
Provide or generate the 5×5 grayscale input image.
Perform the convolution operation using the 3×3 filter.
Apply ReLU activation.
Extract the resulting features.
Apply the Isolation Forest algorithm.
Observe the final anomaly classification.
Applications

The concepts demonstrated in this project can be extended to applications such as:

Image quality inspection
Defect detection
Pattern analysis
Industrial anomaly detection
Computer vision preprocessing
Automated visual inspection
Conclusion

This project demonstrates a basic image anomaly detection pipeline combining convolution-based feature extraction with unsupervised machine learning.

The 5×5 grayscale image is processed using a 3×3 convolution filter to obtain a feature map. The ReLU activation function is then applied to introduce non-linearity and obtain meaningful non-negative features. These features are subsequently analyzed using the Isolation Forest algorithm to identify anomalous patterns.

The project provides a fundamental understanding of how image processing, feature extraction, and machine learning can be integrated to perform anomaly detection.
