# Image-Segmentation-of-Handwritten-Digits

<img src='https://drive.google.com/uc?export=view&id=1-WBX7w_R9abwdGmAUBFWWEcJ0LkMppq2' alt='m2nist digits'>

A model will be built that predicts the segmentation masks (pixel-wise label map) of handwritten digits. This model will be trained on the [M2NIST dataset](https://www.kaggle.com/farhanhubble/multimnistm2nist), a multi digit MNIST.

## Define the FCN-8 decoder
Now the upsampling path can be defined by taking the outputs of convolutions at each stage as arguments. This will be very similar to what you did in the ungraded lab (VGG16-FCN8-CamVid) so you can refer to it if you need a refresher. 
* Note: remember to set the `data_format` parameter for the Conv2D layers. 

Here is also the diagram you saw in class on how it should work:

<img src='https://drive.google.com/uc?export=view&id=1lrqB4YegV8jXWNfyYAaeuFlwXIc54aRP' alt='fcn-8'>

### Metrics

We showed in the lectures two ways to evaluate your predictions. The *intersection over union (IOU)* and the *dice score*. Recall that:

