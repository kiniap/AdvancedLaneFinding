# AdvancedLaneFinding

This uses advanced computer vision techniques to identify lanes lines in images or videos from a car driving along the road. Identifying the lane lines will help a self driving car identify the boundaries within which it needs to operate.

The following steps have been taken, which have been combined into a image processing pipeline that can used to detect lane lines in a video
1. Calibrate the camera to get the camera matrix
2. Undistort the image using the camera matrix
3. Use a combination of color and gradient thresholding to identify the lane lines in the image
4. Apply a perspective transform the get a bird's eye view of the image
5. Use radius of curvature, center offset, and other features to sanity check the detected lane lines
6. Combine all the various steps into an image processing pipeline to reliably detect lane lines
7. Finally apply the image processing pipeline on a video output from the camera

The detailed steps along with example images is in the AdvancedLaneFinding.ipynb Jupyter notebooks

`jupyter notebook findLaneLinesOnRoad.ipynb`

To execute the notebook the following packages are needed:

* OpenCv
* Numpy
* MatplotLib
* MoviePy

## Output

Ouput video with the lane area marked on the video images is include in the video_output folder: project_video_out.mp4
