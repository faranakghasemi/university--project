# university--project
cardiac Atrium Segmentation Using U-Net

This project is a deep learning-based approach for segmenting the atrium in cardiac DICOM images using a U-Net architecture. It includes preprocessing of medical DICOM files, model construction, training, and visualization of results.

📂 Project Overview
This notebook performs the following tasks:

Loading and Preprocessing DICOM Images

Reads a series of DICOM files from a CT or MRI scan.

Resizes and normalizes them for model input.

U-Net Model Construction

Builds a U-Net architecture tailored for binary segmentation.

Training

Trains the model using available image-mask pairs.

Saves checkpoints and uses early stopping for better generalization.

Prediction & Visualization

Applies the trained model to test slices.

Visualizes predicted masks alongside original DICOM images.

🧪 Dataset
The dataset consists of DICOM slices from DICOM Library.

Images are resized to 256x256 for model compatibility.

Ground truth masks were either provided or generated manually.

Note: This project currently assumes masks are available and match the original image filenames. If masks are missing, additional annotation is required.

📦 Requirements
Python 3.10

tensorflow

pydicom

opencv-python

matplotlib

numpy

Install dependencies with:

pip install -r requirements.txt
Or manually:

pip install tensorflow pydicom opencv-python matplotlib numpy
🧠 Model Architecture
The U-Net model consists of:

Contracting path: repeated Conv2D + MaxPooling2D layers

Expanding path: UpSampling2D + concatenate

Output: 1 channel mask prediction using sigmoid activation

🏁 Results
Trained on 361 slices.

Input shape: (256, 256, 1)

Validation accuracy and loss monitored.

Final output: predicted segmentation mask overlaid on original CT slice.

📌 Future Work
Improve mask quality using better annotation.

Support for 3D segmentation.

Integration with real-time DICOM viewers.

Test on multiple organs or structures.

🧑‍💻 Author
Faranak

GitHub:Faranakghasemi
