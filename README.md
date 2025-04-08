# image-inversion
## Motivation:
Inverting the pixels of each image in a library of images is simple mathematically but can become slow and memory-intensive if not implemented carefully. Assuming each image is treated independently, and the order of image processing does not matter, this task is a good candidate for multithreading with Dask because it is "embarassingly parallel". However, multithreading introduces some overhead, which, for small datasets, can actually slow things down. Here, I will perform pixel inversion using the following 3 methods:

1. For loops
2. Vectorized calculations with Numpy
3. Multithreaded & vectorized calculations with Dask  

For each method, I will conduct time tests across different sample sizes, to understand the benefits of vectorization, and to find out when Dask's overhead becomes worth it.

I use the [kaggle flower image dataset](https://www.kaggle.com/datasets/aksha05/flower-image-dataset?resource=download). 

