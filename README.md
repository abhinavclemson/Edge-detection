
# Basic image convolution and edge detection


	Name: ABHINAV SINGH 
	COURSE ID : CPSC-6820 
	Section number :003 


## Background 

**What is an Edge?**

Area where there are extreme differences in the intensities of the pixel usually indicate an edge of an object.



### Edge Detection using the Sobel-Feldman Edge:

**Detecting edges on an image using separable 1-D Sobel operators(kernels).**

Sobel is very common operator to detect edges of an image, which is an approximation to a derivative of an image. It is separate in the y and x directions. Here Separable kernels are used for optimization, two 1-D arrays as kernels instead of a 2-D matrix, one array is  x and another for y direction. Since multiplying one 1-D row kernel to another 1-D column kernel gives same 2-D kernel, so the original image array is multiplied with row kernel then the resultant matrix to column kernel.

Sobel operator is used for detecting edges by calculating vertical and horizontal gradients, for both of them two separate 1-D kernels, that makes total of four separate 1-D kernels.





##Steps in program
1. An image input is given that is of **pgm** type, which is in greyscale and has pixel values between 0-255.
2. Its values are copied in a 2-D array of float type.
3. Applying two 1-D arrays as kernels on the 2-D array the image array is convoluted, giving output a horizontal or vertical gradient value, according to which gradient is requested.
4. The output is unnormalized 2-D float array, which has pixel values in the resultant array can be less than 0.0 or greater than 255.0.
5. the files dximg.pgm and dyimg.pgm are files that are unnormalized horizontal and vertical gradient edge images respectively.
6. The unnormalized arrays that are stored in dximg.pgm and dyimg.pgm are then scale between 0-255 pixel values and then converted from float type to unsigned integer of 8 bits type as pgm file supported pixel values between 0-255.
7. After scaling the unnormalized arrays are normalized.
8. These new arrays which are normalized are then stored into two new files ndximg.pgm and ndyimg.pgm are files that are normalized horizontal and vertical gradient edge images respectively.
9. All output files are stored in /Output/ directory and input images are took from /Imaged


## 
## Lessons learned, identified interesting features of your program 


## Any special usage instructions 