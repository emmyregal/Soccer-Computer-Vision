# VT Men's Club Soccer Computer Vision

This project is for stat3274, introduction to sports analytics. For this project, we went and 
collected 35 videos of the men's club soccer team taking penalty kicks. These kicks were all 
recorded on the same device, at the same angle, and at the same location via a tripod. 

Once we collected this data, I cleaned and processed the data manually, by cropping the videos down
to just contain the actual motion of the run up of the penalty kick and then a second after it hit
the net. This saved us time computationally for overlaying the YOLO26 model onto each video. 

Once each video was cropped, I overlayed the YOLO 26 pose estimation model ontop of each video. extra
info about YOLO26 can be found here: https://docs.ultralytics.com/models/yolo26 
I made a folder called 'pose_results' which stores the video with the model overlayed ontop of it, 
along with a .csv file that represents some of the key data points we were able to extract from 
the model frame by frame. 

The .ipynb file contains the code that was used to overlay the model and extract certain features and calculate angles based on those features. This file also contains code that was used to manually mark the frame when individual players made contact with the ball and when the ball crossed over the goal line/made contact with the net. Due to the fact that we only had one camera, we were unable to set up multiple angles to observe when the ball crossed over the plane of the goal. This code calculates an estimate of the speed of the ball. We will use this in our analysis. 

## Future Goals
We will analyze if certain metrics or pose angles can help contribute to the speed of the ball. Our goal is to help VT men's soccer improve their penalty kick ball speed. We will report our findings into the .pptx file 
