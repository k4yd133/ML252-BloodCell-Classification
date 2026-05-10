# MACHINE LEARNING (CO3117) - BLOOD CELL CLASSIFICATION

## General Information
* **Course:** Machine Learning (CO3117)
* **Semester:** Semester I - Academic Year 2025–2026 - Class CC01
* **Instructor:** Dr. Truong Vinh Lan

## Project Team (Group 08)
| Full Name | Student ID | Email |
| :--- | :--- | :--- |
| Hoang Minh Cam Tu | 2353289 | tu.hoangkd25@hcmut.edu.vn |
| Pham Hong Minh Tu | 2353293 | tu.phampminhtu787@hcmut.edu.vn |
| Thai Thien Hai Long | 2352699 | long.thaithienhai@hcmut.edu.vn |
| Be Nguyen Dang Khoa | 2352548 | khoa.beyondlimit@hcmut.edu.vn |
| Tran Nguyen Giap | 2352284 | giap.trannguyen@hcmut.edu.vn |

## Project Objectives
This project focuses on automating the classification of four core white blood cell (leukocyte) subtypes in the immune system: Eosinophil, Lymphocyte, Monocyte, and Neutrophil, using microscopic images. 

The primary objectives include:
* **Implementing a Traditional Machine Learning Pipeline:** Exploratory Data Analysis (EDA), data pre-processing (noise removal via IQR analysis), feature extraction (HOG, SIFT-BoVW, PCA), and training traditional classifiers (SVM, Random Forest, k-NN, Logistic Regression, Naive Bayes).
* **Deploying a Deep Learning Approach (Bonus Section):** Utilizing Transfer Learning with pre-trained Convolutional Neural Networks (ResNet-50 and MobileNetV2) to extract high-dimensional spatial features. These are then combined with traditional classifiers for comparative analysis and accuracy maximization (achieving a peak accuracy of 97.07%).

## Project Directory Structure
The project is organized following software engineering standards:
* `notebooks/`: Contains the main Google Colab Notebook (`ML_Group8.ipynb`) to execute the entire experimental pipeline from EDA to evaluation.
* `modules/`: Directory for auxiliary Python scripts. *(Note: To ensure independent and seamless execution during a single "Run all" pass, all helper functions have currently been integrated directly into the Colab notebook).*
* `features/`: Stores the extracted feature arrays in `.npy` format (e.g., `X_hog.npy`, `X_mobilenet.npy`).
* `reports/`: Contains the final PDF project report (`CC01_Group8.pdf`).

## How to Run the Notebook
To ensure the notebook runs successfully and automatically from start to finish, please follow these steps:
1. **Open the Notebook:** Access the Colab file via [this link](https://colab.research.google.com/drive/1GNQjA6DmJmMUuNvvSSFbIQ6e0RQ3mO78?authuser=2#scrollTo=piNs4By8cpIL).
2. **Hardware Accelerator Setup (Crucial):** As this project utilizes Deep Learning models for feature extraction, running on a GPU is strictly required to prevent timeouts. On the Colab toolbar, navigate to **Runtime -> Change runtime type**, select **T4 GPU** under the Hardware accelerator dropdown, and click **Save**.
3. **Environment Configuration:** The notebook is pre-programmed to automatically download image datasets. Users do not need to download any files manually.
4. **Execution:** * On the Google Colab toolbar, select **Runtime -> Run all** (or press `Ctrl + F9`).
   * The process of installing libraries, downloading data, extracting features, and training models will run entirely automatically.

> **Important Note:** Mounting your personal Google Drive is not required, ensuring the source code runs seamlessly without being interrupted by authorization steps.