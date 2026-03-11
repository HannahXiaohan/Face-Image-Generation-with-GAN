## Face Aging GAN – Lifespan Age Transformation Synthesis

This project is focused on creating an application that transforms a given face image to appear younger or older using a pre-trained GAN model. The implementation is based on the Lifespan Age Transformation Synthesis repository.

## Demo 
Input Image: 

<img width="296" height="197" alt="image" src="https://github.com/user-attachments/assets/c0476530-932e-4494-a8bb-00056d99d3f0" />

Apply Quantization: 

<img width="260" height="262" alt="image" src="https://github.com/user-attachments/assets/0e5ed23e-977b-47ba-accd-63a90feb99f7" />

Original:

<img width="259" height="263" alt="image" src="https://github.com/user-attachments/assets/f01e2e7b-7c12-4395-9c84-583e9521ee55" />

Apply Pruning:

<img width="254" height="252" alt="image" src="https://github.com/user-attachments/assets/27727481-96f6-48a8-9999-c1d99865be49" />

Running time:

<img width="608" height="80" alt="image" src="https://github.com/user-attachments/assets/0c8f5ff9-6d3f-4d08-8f9a-6f96e1e81ad2" />


By comparing the visualization of the three images, the orginal output has the youngest look, and both pruning and quantization outputs have teeth which look more mature. First, I apply
the pruning to reduce the unnecessary weight of the model and to improve the inference
speed. The model appling pruning has the fastest speed with 0.76 seconds to generate the
image, while the original has the slowest speed to generate the image. Later, Applying the
quantization, I changed the fp32 to fp16, so the model has the smallest size with 34.8MB. the reference time became faster with a speed of 1.24 second compared to the original
speed.

## Task Objective
The objective is to:

Apply age transformation to facial images.

Test the model using personal photos.

Experiment with model pruning and quantization techniques.

Compare the performance and outputs before and after these optimizations.

## Project Workflow
Clone Repository:
git clone https://github.com/royorel/Lifespan_Age_Transformation_Synthesis
!cd Lifespan_Age_Transformation_Synthesis
Install Dependencies:

pip3 install -r requirements.txt
Download Pre-trained Models:

python download_models.py
Run Age Transformation: Use the provided scripts or modify the notebook to apply aging effects to your face image.

Quantization and Pruning:

Pruning is applied to reduce the number of parameters in the network.

Quantization is used to reduce the model size and improve inference speed.

Both techniques are tested to evaluate trade-offs in performance vs. quality.

Dependencies
Python 3.7+

PyTorch

OpenCV

scikit-learn

matplotlib

torchvision

(Installable via requirements.txt.)



Author: Xiaohan Jiang
Date: April 29th 2025
