## MoSIG M2 Fall Semester
**Project 3 22 October 2020**
### Face Detection with a sliding window detector at multiple scales.

The objective for this exercise is to use your best MLP face detector constructed last week to detect
faces at multiple scales using windows from a Gaussian Pyramid. You will first construct a sliding
window face detector using your best MLP, and then optimize this detector using a **full octave
Gaussian Pyramid.**

This exercise is composed of four parts.
1) Write a program to extract and flatten a sliding window from an image over a range of sizes from W x H to 8W x 8H. Each window must be transformed to the standard size of input vector for your MLP face detector from last week . Use your best MLP to label each window as face, or not face. Report precision, recall and computing time for evaluation with the images in folds 9 and 10 of FDDB.



2)Write a program to construct a Gaussian pyramid that transforms an image from FDDB into a
full octave pyramid. Demonstrate the impulse response of your pyramid by creating a 512 x 512
RGB image with a single non-zero pixel at the center position (256x256). Display the contents
of central 13 columns (cols 250 to 262) from row 256 from each channel of each level of your
pyramid. 



3) Adapt your sliding window detector to extract and flatten windows of sizes from W x H to 2W
x 2H from each level of a pyramid, using a scale factor of 1.2. Use this program to detect faces
from all images in your pyramid. 


4) Compare precision, recall and computing time for the face detection from an image and from a pyramid using the images in folds 9 and 10 of FDDB Document your work in the Jupyter Notebook by commenting it and send the .ipynb file to:

James.Crowley@inria.fr, Nachwa.Aboubakr@inria.fr, Yangtao.Wang@inria.fr. Results are due before class on Thursday 5 nov. 

### Concepts
full octave Gaussian Pyramid

half octave Gaussian Pyramid

detect faces by reduce orignial image by one/half, different levels into 


### Questions
1. After using pyramid image , how to detect faces？
2. 如何选择损失函数？激活函数
   
那你要看是中间层的激活函数还是输出层的激活函数。中间层普遍使用relu，输出层激活函数则是要根据任务配合loss来选择。典型的多分类一般是softmax和交叉熵，二分类就是sigmoid和交叉熵典型的回归用linear线性激活函数，loss用mse或者余弦距离其他的任务，图片检索，对话生成，都有各自的loss函数，要看看最新paper学习一个的明出处。

激活函数和损失函数是深度学习领域中的两个重要课题。其实应该加入更多因素，比如网络宽度，网络深度和权重初始化方法等。1、激活函数，提供非线性激活，通常情况下，可以选ReLU。2、损失函数，定义了网络的“任务”，通常情况下，回归任务就是L1和L2，分类任务就是softmax+cross-entropy。李宏毅的课程可以给你更多启示。Train不起了，着急，怎么办？
