# Brain-House-Project
## Project Name : Student ID card validity checker
A project of creating AI/ML model to analyze the validity of Student ID Card.
## My Implementation
### **Object Detection and Text Recognition using LSTM and EasyOCR**

This project implements a pipeline for object detection and text recognition using LSTM and EasyOCR. The aim is to extract text from images, classify it into relevant fields, and evaluate the results. The system uses a neural network model to classify the extracted text into predefined categories.

---

## **Table of Contents**
1. [Project Overview](#project-overview)
2. [Prerequisites](#prerequisites)
3. [Dataset](#dataset)
4. [Model Architecture](#model-architecture)
5. [How to Run](#how-to-run)
6. [Results](#results)
7. [Contributing](#contributing)
8. [License](#license)

---

## **Project Overview**

This project uses images with annotations to extract relevant fields such as student names, university names, and expiry dates from ID cards. The solution involves:
- **Image Processing**: Detecting bounding boxes and reading text from regions of interest.
- **Text Classification**: Using an LSTM-based model to classify the extracted text into specific categories (like name, university, etc.).

---

## **Prerequisites**

Ensure you have the following installed:
- Python 3.7+
- TensorFlow
- OpenCV
- EasyOCR
- NumPy
- Pandas

You can install the required packages by running:

```bash
pip install -r requirements.txt
```
## **Dataset**

The dataset used in this project consists of images with annotated bounding boxes, which contain relevant fields such as student names, university names, and expiry dates. Each image is accompanied by a JSON annotation file that contains the coordinates of the bounding box and the text inside the box.


- **DATA/**: This folder contains all the images you want to process.
- **Annotation/**: This folder contains corresponding annotation files in JSON format, where each file has the same name as its corresponding image.

### **Annotations Format**

Each annotation file (in JSON format) includes the following information:

```json
{
  "filename": "image1.png",
  "regions": [
    {
      "shape_attributes": {
        "name": "rect",
        "x": 100,
        "y": 200,
        "width": 300,
        "height": 150
      },
      "region_attributes": {
        "field": "student_name",
        "text": "John Doe"
      }
    }
  ]
}
```
-shape_attributes: Contains the bounding box coordinates (x, y, width, height).
-region_attributes: Includes the field name (e.g., student_name, university_name) and the corresponding text inside the bounding box.

### **Downloading the Dataset**

You can download the dataset from [this link](https://example.com/download-dataset) (replace with the actual URL).

Alternatively, you can create your own dataset by following the structure mentioned above. The dataset should contain images and corresponding annotation files in JSON format, organized into `DATA/` and `Annotation/` folders, respectively.

