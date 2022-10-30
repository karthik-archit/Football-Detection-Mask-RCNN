# Football-Detection-Mask-RCNN

Overview:
Object detection and masking of object using Mask R CNN using an keras implementation of Mask RCNN from git : https://github.com/matterport/Mask_RCNN. In this project , I have fine tuned the Mask RCNN model pre-tained on coco weights for a custom dataset to detect footballs in images and videos. Relevant Images from the internet are chosen and are annotated using an online annotation tool. Annotaion tool returns a VGG format json file , contained the all x-axis points and y-axis points, type of mask used and corresponding labels as well. The model is trained on the custom dataset and inference is implemented on test image and video files.

Dataset Used:

Custom football images from the internet.

Libraries Used :

Keras , Tensorflow, Open CV, Numpy , Skimage, Matplotlib, Mrcnn(keras implementation of mask rcnn)

Project Flow:

Training and Evaluation:

Collection of Images -> Annotating images -> Subclassing the Dataset class of mrcnn and updating it according to our dataset -> Loading the model with the our custom config -> Loading coco weights into the model -> Train the model

Inference: 

Create a new inference config by subclassing the config class(setting class properties) -> Importing the custom football dataset -> load the model with trained weights from the recent checkpoint -> detect the feeded input and apply appropriate processing based on whether the input is an image or video file.

Custom Dataset :

A custom dataset class is created by subclassing the parent Dataset class of mrcnn. New image objects of this class is created with appropriate labels from the annotation file. Masks are loaded onto these images from the annotation.
This project enabled me to explore annotating images to create our own custom datasets based. Subclassing the parent class to modify it according to train them on our datasets. Visualizing the model detection, applying the mask and bounding boxes on the input image or video. Also helped me understand the architecture and intuition that led to the Mask RCNN model. Studies the concept of bounding box regressors and how bounding boxes are proposed in the initial stages.

