# skimage
pic analysis
#cmd
# pip install numpy
# pip install scikit-image
# pip install matplotlib

import numpy as np
from skimage.io import imread
from skimage.color import rgb2lab, lab2rgb
import matplotlib.pyplot as plt

# image path

im = imread('images\D:....\color.jpg')

# color space lab

im1 = rgb2lab(im)
im1[...,1] = im1[...,2] = 0
im1 = lab2rgb(im1)

# image size , title , plotting

plt.figure(figsize=(20,10))
plt.subplot(121),plt.show(im),plt.axis('off'),plt.tittle('original image' , size=20)
plt.subplot(122),plt.imshow(im1),plt.axis('off'),plt.title('Grayt Scale Image', size=20)
plt.show()


