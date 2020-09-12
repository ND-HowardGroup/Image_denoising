# Image_denoising
This is the github location for image denoising ImageJ tool and its source codee
#Author: Varun Mannam
#Contributors: Yide Zhang
#Details: The Department of Electrical Engineering, The University of Notre Dame, South Bend, Indiana (IN), USA. Zip: 46556
#email: vmannam@nd.edu
paper: Instant Image Denoising Plugin for ImageJ using Convolutional Neural Networks
https://www.osapublishing.org/abstract.cfm?uri=Microscopy-2020-MW2A.3

#Images: The test images can be downloaded from here https://curate.nd.edu/show/f4752f78z6t

#Citation for dataset: Please cite the FMD dataset using the following format: 
Mannam, Varun, Yide Zhang, and Scott Howard. “Fluorescence Microscopy Denoising (FMD) Dataset.” Notre Dame, April 21, 2019. https://doi.org/10.7274/r0-ed2r-4052.
#DOI: 10.7274/r0-ed2r-4052


Description: This is the plugin used to denoise any fluorescence microscopy image that contains combination of Poisson-Gaussian noise. This algorithm is developed by training the noisy microscopic images with the convolutional neural networks using the U-Net architecture.

Steps to get a denoised image:
1a. Open Fiji/ImageJ
1b. ImageJ -> Edit -> Options -> Tensorflow -> Choose the Tensorflow TF version based on the user system requirements (like: CPU or GPU with proper CUDA drivers)
2. Select an image in ImageJ (use open image function: File ->open)
3. Run the image-denoising plugin (Plugins -> Image denoising -> U-Net denosing) then denoised image will pop-up.  (by default denoised image is 32-bit float type and use ImageJ to combine the color images or other functions)
4. Use the console to check for the test time.


Limitations:
1. Plugin is  limiteed in the number of images at a time to denoise (limitation on the TF memory)
2. If the image size is not multiple of 32x32, linear interpolation is used before passing through the model and again resized to the original image dimension.
3. Speed is better in presence of GPU machine compared to the CPU version.
4. 4D images support is not added yet this stage.
5. GPU common errors are linking the CUDA drivers using symbolic names.

## **Copyright**

© 2019 Varun Mannam, University of Notre Dame  

## **License**

Licensed under the [Apache License 2.0](https://github.com/ND-HowardGroup/Image_denoising/blob/master/LICENSE.txt)

