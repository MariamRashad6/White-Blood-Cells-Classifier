# White Blood Cell Segmentation and Classification

This project aims to develop a program for the automated segmentation of white blood cells (WBC) in images using OpenCV and Python. The program takes a WBC image as input and produces a binary image with only the white blood cell (the purplish object) as output. The dataset for testing and evaluation is provided in a zip file named "Dataset_Pre". In addition to segmentation, the program also includes feature extraction and classification steps.

## Installation

To run the program, ensure that you have the following dependencies installed:

- Python (version 3.6 or higher)
- OpenCV (version 4.0 or higher)
- NumPy (version 1.19 or higher)
- Scikit-learn (version 0.24 or higher)

You can install the necessary packages using pip, the Python package manager. Open your terminal and run the following command:

```
pip install opencv-python numpy scikit-learn
```

## Usage

1. Download and extract the "Dataset_Pre" zip file, which contains the WBC images for testing and the ground truth for evaluation.

2. Clone this repository or download the source code files.

3. Place the WBC images in the same directory as the project files.

4. Open a terminal and navigate to the project directory.

5. Run the following command to preprocess the images, perform segmentation, extract features, and train the classifier:

   ````
   python wbc_segmentation_classification.py
   ```

   The program will process all the images in the dataset and generate the segmented binary images using various techniques such as contrast adjustment, noise removal, thresholding, and morphological operations.

   After segmentation, the program will extract features such as area, perimeter, circularity, eccentricity, invariant moments, and Fourier descriptors from the segmented white blood cells.

   Finally, the program will split the feature table into training and testing sets using an 80% training - 20% testing ratio. It will train a classifier using the training set and evaluate its accuracy on the testing set.

6. Check the program's output in the terminal. It will display the accuracy of the segmentation and classification steps, along with any relevant information or errors encountered during execution.

7. Review the generated reports, which include source code snippets, explanations of each function used, intermediate images after each processing step, IoU segmentation accuracy metrics, and the trained classifier's accuracy figures.

## Customization

You can customize the program to suit your specific requirements. Here are some possible customizations:

- **Preprocessing:** If you want to modify the preprocessing steps such as image denoising, contrast enhancement, or image sharpening, you can edit the code in `wbc_segmentation_classification.py` and add or modify the corresponding functions.

- **Segmentation Techniques:** The program currently uses thresholding and morphological operations for segmentation. If you want to explore other techniques like watershed, region growing, or other segmentation algorithms, you can modify the code in `wbc_segmentation_classification.py` and add or replace the segmentation functions accordingly.

- **Feature Extraction:** If you wish to include additional features or modify the feature extraction process, you can edit the code in `wbc_segmentation_classification.py`, specifically the `extract_features` function. You can add or remove feature calculations based on your requirements.

- **Classification Algorithm:** The program uses the scikit-learn library to train and test a classifier. If you want to use a different classification algorithm or adjust the parameters, you can modify the code in `wbc_segmentation_classification.py` and replace the classifier or update its settings accordingly.

## Contributing

If you encounter any issues, have suggestions for improvement, or would like to contribute to this project, please feel free to open an issue or submit a pull request on the GitHub repository.

## License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute the code as per the terms of the license.

---
Note: This README assumes that you have a basic understanding of Python, image processing, and machine learning concepts. If you need further assistance, please refer to the official documentation of OpenCV, scikit-learn, or consult relevant resources.
