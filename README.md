# A new approach for Image Super Resolution 
A new approach for Image Super Resolution using Convolutional Neural Networks.
## 1. Basic Idea
Sliding Window Technique: 

Input Image => 5x5 patch => Model => 10x10 patch => Full Super-Resolution Image

<img src="data_sample/input_output.jpg" width="800">

<img src="data_sample/input_output_cr7.jpg" width="800">

## 2. Problem of Sliding Window
Grid appears in the produced output.

<img src="data_sample/slidingwindowproblem.png" width="800">

## 3. Solution
Use smaller stride steps than the window size, and use only the center region to produce the super resolution.
<img src="data_sample/sw_solution.png" width="800">

The difference between stride step of 5 and 3.

<img src="data_sample/stride_5_3.png" width="800">

Last Update in Nov. 2019

Tran Le Anh
