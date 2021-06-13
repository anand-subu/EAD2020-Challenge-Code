# EAD2020-Challenge-Code
Code for our EAD2020 Challenge Attempt (https://ead2020.grand-challenge.org/)

This repo will host the code for our solution of the EAD-2020 challenge as described in our [paper](http://ceur-ws.org/Vol-2595/endoCV2020_paper_id_22.pdf).

The main code resources hosted here are the data generator scripts used while training the semantic segmentation network, and the inference files for the objection detection and semantic segmentation tasks.

## Guidelines for any general queries:
  * `AttributeError: module 'keras.utils' has no attribute 'generic_utils'` - This could be due to both keras and tf.keras present in the python environment. Refer to the [readme file of the segmentation_models repository](https://github.com/qubvel/segmentation_models), specifically in terms of how to set environment variable to avoid this issue.
    * For Windows environments, try running `set SM_FRAMEWORK=tf.keras/keras` as required.
    * For Linux environments, try running `export SM_FRAMEWORK=tf.keras/keras` as required.
  
  * <b>The Segmentation Data Generator treats images as BGR and pixel values are not rescaled.</b> Refer this [issue in segmentation_models](https://github.com/qubvel/segmentation_models/issues/23) for reasons why it is kept this way for ResNet model backends, specifically since this is with reference to the U-Net Model we used. The preprocessing can be tinkered with easily to work with any other model specific preprocessing requirements.


# Resources:

The following resources were of great assistance to us while developing various components of our solution in our paper, in terms of both motivation, understanding concepts and/or for reusing parts of code from, for which we would like to express our sincere gratitude.

### Object tracking pipeline:
* [OpenCV's Object Tracking Documentation](https://docs.opencv.org/3.4/d9/df8/group__tracking.html)
* [Multi-Object Tracking using Dlib and OpenCV- Adrian Rosebrock (Pyimagesearch)](https://www.pyimagesearch.com/2018/10/29/multi-object-tracking-with-dlib/)
* [Object Tracking using OpenCV - Sathya Mallick (Learn OpenCV)](https://www.learnopencv.com/object-tracking-using-opencv-cpp-python/)
* [Object Tracking APIs OpenCV- Adrian Rosebrock (Pyimagesearch)](https://www.pyimagesearch.com/2018/10/22/object-tracking-with-dlib/)

### Keras Data Generators:

* [A detailed example of how to use data generators with Keras - By Afshine Amidi and Shervine Amidi](https://stanford.edu/~shervine/blog/keras-how-to-generate-data-on-the-fly)

### Segmentation Ensemble Pipeline:

* [Using the EAST Text Detector for text detection- Adrian Rosebrock (Pyimagesearch)](https://www.pyimagesearch.com/2018/08/20/opencv-text-detection-east-text-detector/)

### Object Detection Ensemble Pipeline:
* [Ensemble methods for object detection](https://github.com/ancasag/ensembleObjectDetection)

### Deep Learning Models Used:

* [Deeplab-v3](https://github.com/bonlime/keras-deeplab-v3-plus)
* [Unet](https://github.com/qubvel/segmentation_models)
* [Retinanet](https://github.com/fizyr/keras-retinanet)
* [Faster-RCNN](https://github.com/tensorflow/models/tree/master/research/object_detection)



