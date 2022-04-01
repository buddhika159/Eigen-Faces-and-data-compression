# Eigen Faces and Data compression
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)

## Description:
This Project based on the book [Data-Driven Science and Engineering: Machine Learning, Dynamical Systems, and Control](http://www.databookuw.com/) PART 1 Chapter 1: Singular Value Decomposition. 
In this project we will use Extended Yale Face Database to construct a data compression algorithm using Eigen faces. Steps include:
 - Create a large readable matrix `allPersons` from the data set with each block assigned to each individual
 - Compute the mean (or average) face out all of them and create `avgFace`
 - Compute Eigen Faces (or Eigenvectors) using `np.linalg.svd()`
 - Store `U[:,:r]` as it is the compression weights needs to compress a given image. Then, 
   - one can send a compressed image data `compressed_data = U[:,:r].T*testFace` and 
   - receiver can decompress the data with `U[:,:r]*compressed_data`
 - Compress a given `testFace` by projecting it to the projection matrix `U[:,:r]*U[:,:r].T`

<p align="middle">
  <img src="all_faces.jpeg" width="70%" />
</p>

Below shows the projection of two test faces into the Eigen Face projection matrix by selecting different number of Eigen Faces.

<p align="middle">
  <img src="test_face_1.png" width="70%" />
</p>

<p align="middle">
  <img src="test_face_2.png" width="70%" />
</p>


## Prerequisites:

Below libraries are needed to execute this Python code.
 - numpy
 - matplotlib
