Thursday 22 Oct 2020  Lesson 3:  Scale Space and Image Pyramids (Recorded Lecture) 
Computer Vision Theory
Scale Space
Gaussian function as a low-pass digital filter
Scale Invariant Gaussian  Pyramids
Equivariance Properties of Scale Space
Practical Instruction:  Yangtao Wang's Jupyter Notebook demo
           • Constructing an Image pyramid with OpenCV
           • Detecting Faces at multiple scales with a pyramid
Programming Exercise 3:  Detecting Faces at multiple scales with a pyramid and a sliding window MLP (updated 25 oct)
Background Reading:  Face Detection with Half octave Pyramid (Ruiz 2008)  (Crowley-Riff 2003)


Muti-Scale
Pyramid image
gaussian filter
laplacian


##  Recursive Pyramid Algorithm

## full-octave pyramid
The position in the original image of a sample from level k is  x = i∆xk and y = j∆yk  If we sampling at a scale step of ∆xk = 2k  this gives a  "full octave" pyramid.
## half-octave pyramid
It is also possible to build a scale invariant pyramid with a step size of  ∆xk = 2k/2  using ∆xk  = 2k/2   This is known as a “half-octave” pyramid

## Image Pyramids
https://docs.opencv.org/master/dc/dff/tutorial_py_pyramids.html

We can find Gaussian pyramids using cv.pyrDown() and cv.pyrUp() functions.