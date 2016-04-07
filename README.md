# AI Painting

## Introduction

This repository contains a pyCaffe-based implementation of "A Neural Algorithm of Artistic Style" by L. Gatys, A. Ecker, and M. Bethge, which presents a method for transferring the artistic style of one input image onto another. You can read the paper here: http://arxiv.org/abs/1508.06576. 

Neural net operations are handled by Caffe, while loss minimization and other miscellaneous matrix operations are performed using numpy and scipy. L-BFGS is used for minimization.

## Requirements

 - Python >= 2.7
 - Caffe == latest 
 - CUDA >= 7.0 (highly recommended)
 
## TODOs

  - Verify model_WEIGHTS is working as expected
  - Add progress bar for minimize call

## Download

To run the code, you must have Caffe-Windows pyCaffe installed. Detailed installation instructions for Caffe can be found [here](http://caffe.berkeleyvision.org/installation.html).

Follow the UI instruction, choose you style image, original image and convnet model_name. Here, `<model_name>` must be one of `caffenet`, `googlenet`, or `vgg`.

The protobufs which come with the vanilla Caffe install aren't quite compatible with this code - working ones have already been added to this repository as a result of this.

This will grab the convnet models from the links provided in the [Caffe Model Zoo](https://github.com/BVLC/caffe/wiki/Model-Zoo).

Or you can also download all packaged models from [here](http://pan.baidu.com/s/1pLsyfmN), and replace the .\models folder;

After all of config above, just click Train botton and have fun. All results were generated in around two minutes on an NVidia GeForce Quadro K2200 GPU running the GoogleNet model and 30 minutes with VGG model.
## Sample



<p align="center">
<img src="https://raw.githubusercontent.com/inlmouse/AIPainting/master/images/starry_night.jpg" width="100%"/>
</p>
<p align="center">
<img src="https://raw.githubusercontent.com/inlmouse/AIPainting/master/outputs/fixed.png" width="100%"/>
<img src="https://raw.githubusercontent.com/inlmouse/AIPainting/master/outputs/ha_result_strray_vgg.jpg" width="100%"/>
</p>

You are able to visit more examples in .\outputs.

