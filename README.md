# K-Nearest Neighbors (KNN) Project

This project implements a K-Nearest Neighbors (KNN) classifier to recognize actors based on a dataset of images. The classifier calculates the Euclidean distance between an uploaded image and a dataset of actor images to find the closest matches. The project supports 1NN, 3NN, and 5NN using majority voting for classification.

## Dataset

- The dataset consists of **50 images** of **10 actors** (5 pictures per actor).
- All images are **32x32x3** in size.
- Each image is preprocessed and reshaped into vectors for distance computation.

## Workflow

1. **Data Preprocessing**:
    - The images from the dataset are resized to **32x32x3**.
    - The user uploads their own image, which is also resized to **32x32**.
    - All images (both from the dataset and the user's image) are reshaped into vectors for distance calculation.

2. **Euclidean Distance Calculation**:
    - Euclidean distance is computed between the uploaded image and each image in the dataset.

3. **KNN Classification**:
    - **1-Nearest Neighbor (1NN)**: The image with the smallest Euclidean distance is identified as the match.
    - **3-Nearest Neighbors (3NN)**: The 3 images with the smallest distances are found, and majority voting is used to determine the predicted actor.
    - **5-Nearest Neighbors (5NN)**: The 5 closest images are identified, and majority voting is used to make the prediction.

## How to Use

1. **Clone the repository**:
    ```bash
    git clone https://github.com/siddiquiali94/knn.git
    ```

2. **Install the necessary libraries**:
    This project requires `numpy`, `matplotlib`, and any image processing library you are using (e.g., `opencv` or `PIL`). Install them using:
    ```bash
    pip install -r requirements.txt
    ```

3. **Run the project**:
    The project script will guide you through uploading your image and performing KNN classification:
    ```bash
    knn.py
    ```

## Files

- `knn_classifier.py`: The main Python script implementing the KNN algorithm and processing the images.
- `data/`: Directory containing the raw images of actors.
- `README.md`: Documentation for the project.
- `requirements.txt`: List of dependencies for the project.

## Example

Once you upload an image, the KNN classifier will output the nearest neighbor's label and display the corresponding images from the dataset. It will also perform 3NN and 5NN classification using majority voting.

## Future Improvements

- Support for larger datasets.
- Addition of other distance metrics like Manhattan distance.
- Integration of a graphical interface for image upload and display.

