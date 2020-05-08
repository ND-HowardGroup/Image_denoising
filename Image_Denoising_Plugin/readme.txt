Paper: Instant Image Denoising Plugin for ImageJ using Convolutional Neural Networks
link: https://www.osapublishing.org/abstract.cfm?uri=Microscopy-2020-MW2A.3

#Author: Varun Mannam
#Contributors: Yide Zhang
#Details: The Department of Electrical Engineering, The University of Notre Dame, South Bend, Indiana (IN), USA. Zip: 46556
#email: vmannam@nd.edu

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


