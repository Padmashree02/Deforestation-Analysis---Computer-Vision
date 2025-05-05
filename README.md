# Application -> Image Segmentation
# 1. Measure the presence of vegetation (forest areas) in the satelite images (normal format) for the years 1985 | 1993 | 2001 | 2011.

# 2. Analysis and compare the RGB type image with HSV type channel image.

Libraries - cv2, numpy, matplotlib

Language - Python

Topics - BGR (RGB) channel and HSV channel, Histogram (Linear and Log scale), Inrange mask, Image segmenation

Pipeline -

    > Read the images
  
    > Pre-processing :-
  
        * Split the each images into three channels - B G R
        
        * Plot the histogram of each year of images and using histogram, analysis the image - understand the range of pixels whose intensities are at the highest peak.
        
        * Set the lower and upper values using histogram, which will be used while forming the mask.
        
    > Pass the origional (color image) image of each years into the inrange function by setting the lower and upper value (as per the image).
   
    > The mask will be in the form of white and black image - where white values of pixels represents the forest area and black values of pixels as roads or non-forest area.
   
    > Post-preprocessing :-
  
        * From the mask, calculate the green part by calculating the number of pixels that are non-zero (255=white).
  
    > To compare with HSV type images.
  
    > Pre-processing :-
  
        * Convert the image of each years into HSV channel.
  
        * Split the each images into three channels - H S V
        
        * Plot the histogram of each year of images and using histogram, analysis the image - select the range of pixels whose intensities are at the highest peak in each channel.
        
        * Set the lower and upper values using histogram, which will be used while forming the mask.
        
    > Pass the origional (HSV image) image of each years into the inrange function by setting the lower and upper value (as per the image).
   
    > Post-processing :-
   
        * calculate the green part by calculating the number of pixels that are non-zero (255=white).

Result -

  > The percentage of vegetation of each years from RGB channel is different from HSV channel images.
 
  > From RGB the values are higher than from HSV, thus analysis the deforestation or any images using HSV channel of image gives accurate results as HSV splits the images into Hue, saturation and values (each color accurately distributes in each channel). 
