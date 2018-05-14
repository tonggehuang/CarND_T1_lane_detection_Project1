# CarND_T1_lane_detection_Project1

## Reflection

### 1. Pipeline Description

###    1.1 Image Preprocessing
###         1.1.1 Color images to gray scale.
###         1.1.2 Gaussian kernel smooth the gray image.
###         1.1.3 Canny function detect the edge (low threshold = 5, high threshold = 150, 2:3).
###     1.2 ROI Mask
###         1.2.1 Mask the interest lane detection area based on image dimensions.
###     1.3 Lane detection & extrapolate (extrapolate_lane function)
###         1.3.1 Finding the possible lane segments with Hough Transform.
###        1.3.2 Left lane and right lane are seperated by slope (m<0,m>0)
###         1.3.3 Calculating the average slope and intercepts to extrapolate the entire lane.(Detail showed above)
###     1.4 Generating a single, solid line (extrapolate_lane function)
###         1.4.1 Smoothing the line by using the lines generated from previous frames.(storage size = 5) Updating the current line location to genetate single, solid line.
###         1.4.2 Drawing the two detected red lines for each frame. (draw_lines,weighted_img function) 
###        
### 2. Potential Shortcomings
###     
###     2.1 ROI selection: 
###         The ROI are selected by hands. It might not be fitted for other images or videos. 
###     2.2 Hough transform parameters: 
###         Setting the hough transforma parameters is hand-craft in this pipeline, it might not be fitted for other   tasks.
###     2.3 Curve:
###         This pipeline did not work very well in challenge video, which contains the curve lane. Also, the shadow of other car, barriers will effect the accuracy of lane detection. 
        
### 3. Possible Improvement:
    
###     3.1 Automatic ROI generation algorithm
    
###     3.2 Instead of simply change color image to gray scale, the yellow lane, with lane could be picked out by filtering certain channels, so that the shadow of other object will not effect the lane detection. 
 
