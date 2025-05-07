# Application 1 -> Image Segmentation
# 1. Measure the presence of vegetation (forest areas) in the satelite images (.jpg or .png) for the years 1985 | 1993 | 2001 | 2011.

# 2. Analysis the vegatation understanding the image's pixel values through RGB channel.

Libraries - cv2, numpy, matplotlib

Language - Python

Topics - BGR (RGB) channel, Histogram (Linear and Log scale), Inrange mask, Image segmenation

Pipeline -

    > Read the images
  
    > Pre-processing :-
  
        * Split the each images into three channels - B G R
        
        * Plot the histogram of each year of images and using histogram, analysis the image - understand the range of pixels whose intensities are at the highest peak.
        
        * Set the lower and upper values using histogram, which will be used while forming the mask.
        
    > Pass the origional (color image) image of each years into the inrange function by setting the lower and upper value (as per the image).

Result -

  > The percentage of vegetation of each years from 1985 to 2011 is gradually decreasing, perhaps due to climate change effect, deforestation for urban development etc.
 
   
    > The mask will be in the form of white and black image - where white values of pixels represents the forest area and black values of pixels as roads or non-forest area.
   
    > Post-preprocessing :-
  
        * From the mask, calculate the green part by calculating the number of pixels that are non-zero (255=white).
