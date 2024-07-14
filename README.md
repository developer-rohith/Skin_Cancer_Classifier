# Skin Cancer Lesion Classifier

This project aims to classify skin cancer lesions into 7 different classes using deep learning techniques. It utilizes the HAM10000 dataset, which contains various types of skin lesions.

## Dataset
- **Dataset Source**: [HAM10000 Dataset on Kaggle](https://www.kaggle.com/kmader/skin-cancer-mnist-ham10000)
- **Description**: The dataset consists of images of skin lesions categorized into 7 classes:
  1. Melanocytic nevi (nv)
  2. Melanoma (mel)
  3. Benign keratosis-like lesions (bkl)
  4. Basal cell carcinoma (bcc)
  5. Actinic keratoses (akiec)
  6. Vascular lesions (vas)
  7. Dermatofibroma (df)

## Tools and Technologies Used
- **Python Libraries**:
  - Flask for building the web application
  - TensorFlow and Keras for developing and training the deep learning model
  - NumPy, Pandas, and Matplotlib for data manipulation and visualization
- **Docker**: Containerization of the application for easy deployment
- **HTML/CSS**: Front-end interface for uploading images and displaying results

## Model Training
- **Model Architecture**: Convolutional Neural Network (CNN) using TensorFlow/Keras
- **Training**: The model is trained on resized images (32x32 pixels) from the HAM10000 dataset. Data augmentation techniques are applied to enhance model performance.

## Usage
1. **Clone Repository**: Clone this repository to your local machine.
2. **Install Dependencies**: Ensure Python dependencies are installed using `requirements.txt`.
   ```bash
   pip install -r requirements.txt
   ```
3. **Run Application**:
   - Build the Docker image:
     ```bash
     docker build -t skincancer-app .
     ```
   - Run the Docker container:
     ```bash
     docker run -p 5000:5000 skincancer-app
     ```
   - Access the application in your browser at `http://localhost:5000`.

4. **Upload Images**: Upload a skin lesion image through the web interface and click submit to classify the lesion.

