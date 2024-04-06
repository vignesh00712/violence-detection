# violence-detection
Violence Detection is a cutting-edge technology leveraging machine learning and computer vision to automatically identify aggressive or harmful behavior in various media forms. This GitHub repository hosts the codebase and resources essential for implementing and deploying violence detection systems across different applications and platforms.

Table of Contents

    Introduction
    How to Run
    Results
    Future Work

<a name="introduction"/>
Introduction

This repository contains code for a Deep Learning-based algorithm designed to detect violence in both indoor and outdoor environments. The algorithm achieves high accuracy in identifying various scenarios, including fights, fires, car crashes, and more.

To enable detection of additional scenarios, you can simply add descriptive text labels for the scenarios in the settings.yaml file under the labels key. Currently, the model can detect 16 scenarios plus one default "Unknown" label. You have the flexibility to customize, add, or remove labels based on your specific use case.

The model is trained on a diverse range of data, with the primary task being to predict similar vectors for both images and descriptive text that effectively describe the scene depicted in the image. As a result, the model demonstrates good generalization capabilities for detecting various scenarios when provided with appropriate textual information about the scene of interest.
<a name="how-to-run"/>
How to Run
Installation

First, install the required dependencies:

pip install -r requirements.txt

Testing the Model

You can test the model using one of the following methods:

    Run the model on a single image:

    arduino

python run.py --image-path ./data/7.jpg

Test the model through the web application:

arduino

streamlit run app.py

Use the provided Jupyter notebook tutorial.ipynb for a step-by-step example.

Integrate the model into your project using the provided code snippet:

python

    from model import Model
    import cv2

    model = Model()
    image = cv2.imread('./your_image.jpg')
    image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
    label = model.predict(image=image)['label']
    print('Image label is: ', label)

<a name="results"/>
Results

Below are the resulting videos and images showcasing the model's predictions. The model was applied to each frame of the videos, and the predictions were printed on the left side of the frame. In the case of images, the titles represent the model's predictions. For the code used to produce these results, refer to the tutorial.ipynb Jupyter notebook.
Result Videos

    Result video
    Result video

Result Images

    Result image
    Result image
    Result image
    Result image
    Result image
    Result image
    Result image

<a name="future-work"/>
Future Work

For further enhancements such as batch processing support for speedup, returning multiple suggestions, fine-tuning thresholds for specific data, etc., please feel free to contact me:

LinkedIn: linkedin.com/in/vignesh-kumar-m-36050a26b

