
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

## Steps in program
1. An image input is given that is of **pgm** type, which is in greyscale and has pixel values between 0-255.
2. Its values are copied in a 2-D array of float type.
3. Applying two 1-D arrays as kernels on the 2-D array the image array is convoluted, giving output a horizontal or vertical gradient value, according to which gradient is requested.
4. The output is unnormalized 2-D float array, which has pixel values in the resultant array can be less than 0.0 or greater than 255.0.
5. the files dximg.pgm and dyimg.pgm are files that are unnormalized horizontal and vertical gradient edge images respectively.
6. The unnormalized arrays that are stored in dximg.pgm and dyimg.pgm are then scale between 0-255 pixel values and then converted from float type to unsigned integer of 8 bits type as pgm file supported pixel values between 0-255.
7. After scaling the unnormalized arrays are normalized.
8. These new arrays which are normalized are then stored into two new files ndximg.pgm and ndyimg.pgm are files that are normalized horizontal and vertical gradient edge images respectively.
9. All output files are stored in /Output/ directory and input images are took from /Images.
10. Both horizontal and vertical gradients are combined, by adding absolute values(converting negative values to positive values) of horizontal and vertical gradients.
11. combine.pgm is output as combined horizontal and vertical gradients.
12. combine.ppm is output as combined gradients with RGB channels, the values of combine.pgm is weighted randomly between 0.10 and 0.90 and assigned to RGB channels to give a sparkly look to the image.



## Instructions for the user
1. Program is written in Jupyter notebook using python 3.x
2. Original file is in .ipynb format to open it in Jupyter notebook.
3. Additional, .py files are are also attached, if the user wants to open it in python interpreter.
4. As the program is made on Macos, it uses forward slash for accessing directories, and would automatically detect the directory by using os.cwd for getting present working directory. Have to change forward slash to backward slash , if user operating on Windows machine. 
5. backward slash used in ppm*_*write and pgm*_*write, specifically for the variable **file**.
6. for windows user:

           file= os.getcwd()+'/Output/'+file_name
           can be changed to
           file= os.getcwd()+'\Output\'+file_name
7. Comments are provided in the files. Additionally, code snippets are also provided to show results of previous run.



           
## Dependencies
* [Python 3.0.x](https://www.python.org/download/releases/3.0/)
* [NumPy](https://numpy.org/)
* [Pillow](https://pillow.readthedocs.io/en/stable/)


## Technologies
* [Jupyter notebook](https://jupyter.org/)
* Can be used on **Idle**  too.



Both Jupyter notebook file(.ipynb) and python file(.py) is provided.

           

