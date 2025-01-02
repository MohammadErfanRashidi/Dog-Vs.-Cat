
README for Dogs vs Cats Classification on Google Colab

---

Project Overview
This project involves building a binary image classification model using a neural network to differentiate between dog and cat images. The dataset is sourced from the Kaggle competition "Dogs vs Cats", and pre-trained MobileNet V2 from TensorFlow Hub is utilized for feature extraction.

---

Requirements
To execute this project, ensure the following are available:
- Google Colab environment.
- Kaggle API credentials (kaggle.json file).
- Libraries: TensorFlow, NumPy, Pandas, Matplotlib, Scikit-learn, PIL, OpenCV, TensorFlow Hub.

---

Steps to Run the Project

1. Setup Kaggle API
   Install the Kaggle library, upload your kaggle.json file, and configure the API for downloading datasets.
   ```
   !pip install kaggle
   !mkdir -p ~/.kaggle
   !cp kaggle.json ~/.kaggle/
   !chmod 600 ~/.kaggle/kaggle.json
   ```

2. Download and Extract Dataset
   Download the dataset from Kaggle and extract the compressed files.
   ```
   !kaggle competitions download -c dogs-vs-cats
   ```
   Use Python's `zipfile` library to extract images into appropriate directories.

3. Dataset Overview
   - Count the number of images.
   - Preview file names and analyze the dataset distribution (e.g., number of dog and cat images).

4. Preprocessing
   - Resize all images to 224x224 pixels.
   - Convert images to RGB format.
   - Scale pixel values to the range [0, 1].

5. Model Training
   - Use MobileNet V2 from TensorFlow Hub as a feature extractor.
   - Define a neural network model with a Dense layer for binary classification (dog vs cat).
   - Train the model on 80% of the dataset and validate it on the remaining 20%.

6. Evaluation
   - Evaluate the model's performance on the test set.
   - Report metrics like accuracy and loss.

7. Predictions
   - Provide the path to an image to classify it as either a dog or a cat.
   - Display the image alongside the predicted label.

---

Note
- Ensure that the `kaggle.json` file is placed in the appropriate directory with correct permissions.
- Adjust the number of images used during preprocessing if working with limited computational resources.

---

Contact
For questions or issues related to this project, please contact the creator.
