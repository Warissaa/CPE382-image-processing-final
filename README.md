README — Defective Colored Candy Inspection System
Project Overview
This project implements a classical computer vision pipeline for automatic defect detection and counting of colored candies using image processing techniques.
The system performs:
Image preprocessing
Image segmentation
Binary mask generation
Morphological operations
Contour extraction
Feature extraction
Rule-based defect classification
Quantitative analysis
The project was developed in Jupyter Notebook using Python and OpenCV.

Dataset Description
The dataset contains 15 candy images with realistic imaging challenges including:
Uneven illumination
Shadows
Touching objects
Overlapping objects
Blur
Cluttered background
Cracks and defects
Object classes:
Normal candies
Defective candies
Google drive: https://drive.google.com/drive/folders/1Fvadj-hg9VFFjrWw0sRlIuKgn6Baxz82?usp=sharing

Required Libraries
Install the following Python libraries before running the notebook:
pip install numpy opencv-python matplotlib scikit-image scikit-learn scipy


Project Structure
project_folder/
│
├── dataset/
│   ├──input_images/
│   ├──output_images/
│
├── S_66070503481_M2.ipynb
├── README.md


How to Run the Notebook
Step 1 — Open Jupyter Notebook
Run:
jupyter notebook

or
jupyter lab

Then open:
defect_detection.ipynb


Step 2 — Prepare Dataset
Place all dataset images inside the dataset/ folder.
input_images/
output_images/


Step 3 — Run Notebook Cells Sequentially
Run all cells from top to bottom.
Recommended:
Kernel → Restart & Run All


Notebook Pipeline
The notebook performs the following steps:
1. Load Dataset
Read all images
Display dataset samples
2. Preprocessing
Gaussian blur
HSV conversion
3. Segmentation
Two methods are compared:
HSV color thresholding
K-Means clustering
4. Binary Mask Generation
Convert segmentation output into binary masks
5. Morphological Operations
Opening
Closing
Used to:
Remove noise
Fill holes
Improve contour quality
6. Contour Extraction
Detect object boundaries
Count objects
7. Feature Extraction
Extracted features include:
Area
Circularity
Solidity
Aspect ratio
HSV color features
Harris corners
8. Defect Detection
Rule-based classification:
Normal
Defective
9. Evaluation
Outputs include:
Bounding boxes
Object labels
Confusion matrix
Final statistics

Final Outputs
The notebook generates:
Segmented images
Binary masks
Morphology results
Contour visualization
Harris corner detection
Feature visualization
Defect classification results
Confusion matrix
Quantitative measurements
Example:
Total Objects: 86
Defective Objects: 52
Average Object Size: 12458 pixels
Defect Percentage: 60.47%


Important Notes
This project uses classical image processing only.
No deep learning or YOLO-based models are used.
Results may vary depending on lighting conditions and segmentation quality.
Overlapping candies may produce merged contours and counting errors.
