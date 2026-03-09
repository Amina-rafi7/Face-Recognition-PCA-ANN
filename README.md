# Face-Recognition-PCA-ANN
This project implements a robust Face Recognition System from scratch using Principal Component Analysis (PCA) for feature extraction and an Artificial Neural Network (ANN) for classification. It was developed as the capstone project during my Artificial Intelligence Internship at Internship Studio (iStudio).

The system successfully identifies unknown faces by compressing image data into "Eigenfaces," extracting their mathematical signatures, and passing them through a trained Multi-Layer Perceptron (MLP) neural network.

 Tech Stack & Libraries Used
Language: Python

Machine Learning: Scikit-learn (PCA, MLPClassifier)

Computer Vision: OpenCV (cv2)

Mathematical Operations: NumPy, SciPy

Data Visualization: Matplotlib

 How It Works (Methodology)
Data Preprocessing: Images are read, flattened into column vectors, and mean-aligned by calculating and subtracting the "mean face" from the dataset.

Feature Extraction (PCA): The mean-zero data is used to calculate eigenvectors. The faces are then projected onto these vectors to generate Eigenfaces.

Signature Generation: Each face is compressed into a unique mathematical signature based on its projection on the Eigenfaces.

Model Training (ANN): A Backpropagation Neural Network (MLPClassifier) is trained using 60% of these face signatures to learn the patterns of each individual.

Testing & Prediction: For a new/unknown image, the system mean-aligns it, projects it onto the trained Eigenfaces to find its signature, and uses the ANN to accurately predict the identity of the person.
