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
the model frame by frame
