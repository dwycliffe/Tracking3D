# Simulating stereo triangulation of a customer walking through a warehouse in Unity3D

Each second, all cameras take a pictures. That picture is used to estimate the 2D pixel coordinates of the customer. 

This pixel coordinate location is used along with the corresponding camera's intrinsic and extrinsic parameters to create a world space ray. 

Pairs of cameras are used to calculate their ray intersection point to estimate the 3D position of the red sphere. 

Their estimate is visualized through a green sphere with text displaying which two cameras created the estimate. 


[[Simple Tracking Video Demo]](https://vimeo.com/971766248?share=copy)


# Simulated cameras and FOV
![Camera FOVs iin order from left to right: C1, C2, C3 and C4](Media/CameraFOV.png)


# Known Issues 
If the red sphere is not fully visible in the camera image, the center point coordinates will be off leading to incorrect 3D estimates. 
Lag during the picture capture and processing. 
