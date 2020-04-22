# OpenCV-Python-Read-and-Display-Image
In Computer Vision applications, images are an integral part of the development process. Often there would be a need to read images and display them if required. To read and display image using OpenCV Python, we use cv2.imread() for reading image to a variable and cv2.imshow() to display the image in a separate window.

cv2.imread(/complete/path/to/image,flag)
First argument is complete path to the image along with the extension.

Second argument is an optional flag which could be any one of the following :

cv2.IMREAD_COLOR : Loads a color image. Any transparency of image will be neglected. It is the default flag.
cv2.IMREAD_GRAYSCALE : Loads image in grayscale mode
cv2.IMREAD_UNCHANGED : Loads image as such including alpha channel
Returns numpy array, containing the pixel values. For colored images, each pixel is represented as an array containing Red, Green and Blue channels.

Note that the default flag is cv2.IMREAD_COLOR. Hence even if read a png image with transparency, the transparency channel is neglected.

cv2.imshow(window_name, image)
First argument is name of the window that is displayed when image is shown in.

Second argument is the image to be shown in the window.

#Example

import numpy as np

import cv2

img = cv2.imread('/home/saba/Pictures/Saba.jpg')  #reads an image


cv2.imshow('image',img)                           #shows an image

cv2.waitKey(0)

cv2.destroyAllWindows()
