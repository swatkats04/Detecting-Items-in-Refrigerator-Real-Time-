# Detecting-Items-in-Refrigerator-Real-Time-

## About The Project
In this project we will see how to perform real time object detection under the environments of Collab and to be specific we are going to train yoloV3 with custom objects in Collab and perform the object detection with the use of open CV.

## Objective
Performing object detections on the custom images that we used. 
(Which means the model is applied to multiple regions within an image and then the model compute scores to an image at multiple locations and scales, high scores regions of an image are considered as an object is detected)

## Data description

The dataset consists of 5 classes(apple,banana,cake,orange,milk).

## Project Presentation
https://docs.google.com/presentation/d/1R75a0XO8QiATI7CTDPDel-nqbtIoqYfT69kaFeNLAt8/edit#slide=id.gc6f972163_0_0


## Pipeline Overview

To build and test your YOLO object detection algorithm follow the below steps:
 
 1. [Download Images](/1_Download_Images/)
	 - "Download All Images" is a chrome extension
	 - Downloads all images from a web page and packs them into a zip file.
 2. [Image_Annotation](/2_Image_Annotation/)
	 - Install LabelImg
	 - Annotate images
 3. [Training](/3_Training/)
 	- Train your custom YOLO model on annotated images 
 4. [Inference](/4_Inference/)
 	- Detect objects real time using web-cam
	
## Repo structure
+ [`Image_Annotation`](/Image_Annotation/): Scripts and instructions on annotating images
+ [`Result`](/Result/): Video Recording of the Results
 
## Getting Started

### Google Colab Tutorial <a href="https://colab.research.google.com/drive/10pyFNMAntR1CLol_rBtHda92MDu34yEQ?usp=sharing" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>
With Google Colab you can skip most of the set up steps and start training your own model right away. 

### Requisites
The only hard requirement is a running version of python 3.6 or 3.7. To install python 3.7 go to 
- [python.org/downloads](https://www.python.org/downloads/release/python-376/) 

and follow the installation instructions. Note that this repo has only been tested with python 3.6 and python 3.7 thus it is recommened to use either `python3.6` or `python3.7`.

To speed up training, it is recommended to use a **GPU with CUDA** support. For example on [AWS](/2_Training/AWS/) you can use a `p2.xlarge` instance (Tesla K80 GPU with 12GB memory). Inference is very fast even on a CPU with approximately ~2 images per second. If you want to use your own machine, follow the instructions at [tensorflow.org/install/gpu](https://www.tensorflow.org/install/gpu) to install CUDA drivers. Make sure to install the [correct version of CUDA and cuDNN](https://www.tensorflow.org/install/source#linux). 

## Quick Start (Inference only)
To test the object on web-cam run the + [`Project`](/Project/) script in the root folder with:

```bash
python Object_Detection.py
```

The outputs are saved in [`Detecting-Items-in-Refrigerator-Real-Time/Result/Source_Images`](/Result) . This includes:
 - Food Item pictures with bounding boxes around it with confidence scores.
  
