# Edge Hierarchy Super Resolution 

STATUS: UPDATING...

## 0. Relevant Papers and Debugging
[Paper 1: A Comparison between Multi-Layer Perceptrons and Convolutional Neural Networks for Text Image Super-Resolution](https://www.semanticscholar.org/paper/A-Comparison-between-Multi-Layer-Perceptrons-and-Peyrard-Mamalet/9ce1de451daea5eb376952214e22229a4cf75d03)
```bashrc
File: bicubic_error_super_resolution.ipynb
```

[Paper 2: Image Super-Resolution Using Deep Convolutional Networks (SRCNN)](https://arxiv.org/abs/1501.00092)

[Paper 3: Accelerating the Super-Resolution Convolutional Neural Network (FSRCNN)](http://mmlab.ie.cuhk.edu.hk/projects/FSRCNN.html)

[Paper 4: Real-Time Single Image and Video Super-Resolution Using an Efficient Sub-Pixel Convolutional Neural Network (ESPCN)](https://arxiv.org/abs/1609.05158)

[Paper 5: Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network (SRGAN)](https://arxiv.org/abs/1609.04802)

Our:
```bashrc
File: edge_hierarchy_super_resolution_7x7.ipynb
```
## 1. Basic Idea
Sliding Window Technique: 

Input Image => 5x5 patch => CNN Model => 10x10 patch => Full Super-Resolution Image
```bashrc
File: super_resolution_sliding_window.ipynb
```
<img src="data_sample/input_output.jpg" width="800">

<img src="data_sample/input_output_cr7.jpg" width="800">

## 2. Problem of Sliding Window
Grid appears in the produced output.

<img src="data_sample/slidingwindowproblem.png" width="800">

## 3. Solution
Use smaller stride steps than the window size, and use only the center region to produce the super resolution.
<img src="data_sample/sw_solution.png" width="800">

The difference between stride step of 5 and 3:

<img src="data_sample/stride_5_3.png" width="800">

Result (Upscaling Factor = 2):

<img src="data_sample/input_output_sample.jpg" width="800">

Created on Nov. 1, 2019
Last Update on Dec. 30, 2019

Tran Le Anh
