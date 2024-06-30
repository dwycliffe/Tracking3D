# Stereo Triangulation

All cameras in the scene take a picture on a one second loop. That picture is inspected and the average location of the red pixels is extracted.

This pixel coordinate location is used along with the corresponding camera's intrinsic and extrinsic parameters to create a world space ray. 

The ray intersection point is calculated for pairs of sequential cameras to estimate the 3D position of the red sphere. 

Camera estimates are visualized through a green sphere with text displaying which two (or more) cameras created the estimate. 

If multiple camera pairs produce a prediction the average is used. Cameras that are being used in the 3D prediction are shown in green.


[[Simple Tracking Video Demo]](https://vimeo.com/971942725?share=copy)


# Known Issues 
Lag during the picture capture and processing. All File IO and image processing is done in C# and is not optimized.

If the red sphere is not fully visible in the camera image, the center point coordinates will be off leading to incorrect 3D estimates. 



# To Run 
Download zip files and unpack. Use Unity 2023.2.3f1 or higher to launch the project and press play to start the simulation.


