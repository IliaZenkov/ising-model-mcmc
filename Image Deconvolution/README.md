# Image Deconvolution

# This project can be viewed at https://nbviewer.jupyter.org/github/pinech/Py-Projects/blob/master/Image%20Deconvolution/Image%20Deconvolution.ipynb
In this program, I simulate a pinhole camera - we take an object and convolve it with a simple pinhole camera system to produce an image.
In the case of the pinhole camera, the resulting image will be blurred due to the point-spread-function (PSF) of a pinhole camera.

Here, I attempt to deconvolve, i.e. deblur the image from the pinhole camera to obtain back our original object.
In this program, fourier transforms are used to employ convolution theorem for this purpose.
I also use the Richardson-Lucy deconvolution algorithm to demonstrate its superiority to simple fourier deconvolution.

Richard-Lucy Deconvolution: https://en.wikipedia.org/wiki/Richardson%E2%80%93Lucy_deconvolution
