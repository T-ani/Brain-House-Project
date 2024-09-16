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
3. [Model Architecture](#model-architecture)
4. [Dataset](#dataset)
5. [My Work](#my-work)


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
# **Image Text Recognition and Classification using LSTM**

This project uses object detection and text recognition techniques to extract relevant text fields (such as student names, university names, and expiry dates) from ID card images. The extracted text is classified into predefined categories using an LSTM-based model.

## **Model Architecture**

### **Text Classification Model**
The text classification model is an LSTM-based network that processes tokenized text sequences and outputs field predictions. The architecture includes:

- **Embedding Layer**: Maps text tokens into a vector space.
- **LSTM Layer**: Processes sequence data and learns temporal dependencies.
- **Dense Layers**: Outputs predictions for text categories (e.g., student_name, university_name, etc.).

### **Text Extraction**
We use EasyOCR to extract text from images. After extraction, the texts are classified into predefined categories using the trained LSTM model.

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

You can download the dataset from [Dataset](https://github.com/T-ani/Brain-House-Project/tree/main/DATA) 

Alternatively, you can create your own dataset by following the structure mentioned above. The dataset should contain images and corresponding annotation files in JSON format, organized into `DATA/` and `Annotation/` folders, respectively.

## **My Work**
### My Ideas for implementing this work
My main target was to generalize the model.
- I wanted to analyze the test image without any annotation
- My main idea was to finding/extracting the text from the image
- I wanted to finding the patterns of the text and position of the text
  
For these things I wanted to train my model with such kind of data that needed to be contained text annotation and the position of those text.
So, after analyzing I decided to create JSON file for annotation. 

After that I trained my data with these JSON files and images. I tried to implement as much as could do.

### Dataset Collection/Creation
I created the dataset by my own. With the different template of [Canva Visual Suite](https://www.canva.com/id-cards/templates/student/).
- First I created an excel file of 40 entries with 3 coulumns University_Name,Student_Name,Expiry_Date
- From this excel file I took the University_Name, Student_Name, Expiry_Date and manually desinged each and every Student ID Card
- After creating images, I used [VIA Image Annotator](https://www.robots.ox.ac.uk/~vgg/software/via/via_demo.html) for creating JSON file for each and every image file

 

