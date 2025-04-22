Automatic License Plate Recognition using CNN and OpenCV
=========================================================

This project implements a complete pipeline for Automatic License Plate Recognition (ALPR)
using traditional computer vision and a custom-trained Convolutional Neural Network (CNN)
for character recognition.

It detects license plates from vehicle images, segments individual characters,
and predicts the license number.

---------------------------------------------------------
🚘 Example

Input Image:
  - car.jpg — contains the license plate: DL8CAF5030

Predicted Output:
  - 🚘 Final Plate: DL8CAF5030

---------------------------------------------------------
📌 Features

- License plate detection using Haar Cascade (indian_license_plate.xml)
- Image preprocessing with OpenCV (resize, thresholding, morphology)
- Character segmentation via contour detection
- CNN-based alphanumeric character recognition (0–9, A–Z)
- Post-processing to fix common OCR confusions (e.g., J → 3, O → 0)
- Built in Jupyter Notebook; runs in VS Code or Jupyter Lab

---------------------------------------------------------
🧠 Technologies Used

- Python 3.x
- OpenCV
- NumPy
- TensorFlow / Keras
- Matplotlib
- Jupyter Notebook
- Visual Studio Code

---------------------------------------------------------
📂 Folder Structure

license_plate/
├── ALPR_Project.ipynb            -> Main Jupyter notebook
├── car.jpg                       -> Sample input image
├── contour1.jpg                  -> Preprocessed binary plate
├── indian_license_plate.xml      -> Haar cascade classifier
├── final_model.h5                -> Trained CNN model
├── char_segmented_*.png          -> Segmented characters (debug)
├── README.txt                    -> This file
└── requirements.txt              -> Python dependencies

---------------------------------------------------------
🚀 How to Run

1. Clone the repository:

   git clone https://github.com/jaswanth-komatineni/Automatic-license-plate-recognition.git
   cd Automatic-license-plate-recognition

2. Install requirements:

   pip install -r requirements.txt

3. Launch Jupyter:

   jupyter notebook

Then open the notebook `ALPR_Project.ipynb` and run it step-by-step.

---------------------------------------------------------
🧪 Model & Output

- CNN classifies 36 characters: A–Z and 0–9
- Characters are sorted left to right using x-coordinates
- Confused characters (like J, O, B) are corrected post-classification

---------------------------------------------------------
🔧 Requirements

- Python ≥ 3.7
- opencv-python
- tensorflow
- numpy
- matplotlib

To regenerate requirements.txt:
  pip freeze > requirements.txt

---------------------------------------------------------
🙋‍♂️ Author

Jaswanth Komatineni  
GitHub: https://github.com/jaswanth-komatineni

---------------------------------------------------------
📜 License

This project is open-source and intended for educational use only.
