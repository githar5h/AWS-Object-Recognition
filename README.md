# Object Detection with AWS Rekognition

## Overview

This AWS project showcases an object detection pipeline using **AWS Rekognition**, with **Python** and **Boto3**. The application processes images, detects objects, and visualizes results with bounding boxes and labels.

## Key Components

### Object Detection with AWS Rekognition

- **Image Processing**: A Python-based script reads image files and sends them to AWS Rekognition.
- **Object Detection**: AWS Rekognition detects objects and returns labels with confidence scores.
- **Visualization**: The detected objects are highlighted with bounding boxes and labeled using **Pillow**.

The following image shows the object detection output:

![Output 1](screenshots/output1.png)

### AWS Rekognition & Boto3 Integration

- **Client Setup**: Python script initializes an AWS Rekognition client using **Boto3**.
- **Detection Execution**: The image is processed and labels are extracted from AWS Rekognition.
- **JSON Response Handling**: The Rekognition response is parsed to extract object names, bounding boxes, and confidence scores.

### Image Annotation with Pillow

- **Bounding Box Drawing**: The script uses **Pillow** to draw bounding boxes around detected objects.
- **Labeling**: Detected objects are labeled with confidence scores displayed above the bounding boxes.

The following image shows bounding boxes around detected objects:

![Output 2](screenshots/output2.png)

## Tech Stack

- **AWS Rekognition**: Object detection API
- **Boto3**: AWS SDK for Python
- **Pillow**: Image processing library
- **Python**: Programming language

## Challenges Faced

- **AWS Credentials Handling**: Managing IAM user permissions for secure access.
- **Bounding Box Accuracy**: Adjusting coordinates for precise visualization.
- **Text Readability**: Enhancing label visibility using appropriate font sizes and colors.

## Getting Started

### Prerequisites

- AWS account with **Rekognition** service enabled
- Python 3.x installed
- IAM user with **AmazonRekognitionFullAccess** permissions

### Setup Instructions

1. **Clone the Repository**:
   ```sh
   git clone https://github.com/githar5h/AWS-Object-Recognition.git
   cd aws-object-detection
   ```
2. **Create and Activate Virtual Environment** (optional but recommended):
   ```sh
   python3 -m venv env
   source env/bin/activate
   ```
3. **Install Dependencies**:
   ```sh
   pip install boto3 pillow
   ```
4. **Configure AWS Credentials**:
   ```python
   access_key_id = 'your-access-key'
   secret_access_key = 'your-secret-key'
   ```
5. **Run the Object Detection Script**:
   ```sh
   python object_detection.py
   ```

## Querying and Analysis

- The script outputs detected objects and confidence scores to the console.
- Results are visually represented in the generated image.
