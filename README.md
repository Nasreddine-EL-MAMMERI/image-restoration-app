# Image-Restoration-App-using-opencv-and-streamlit
This repository contains a simple application to demonstrate image inpainting using Streamlit, a popular Python library for building web applications for data science and machine learning projects.


![Alt Text](https://github.com/Nasreddine-EL-MAMMERI/image-restoration-app/blob/master/inPaint_output2.jpg?raw=true)

![Alt Text](https://github.com/Nasreddine-EL-MAMMERI/image-restoration-app/blob/master/inPaint_output1.jpg?raw=true)

# Overview
Image inpainting is a technique used to restore missing or damaged parts of an image. This application allows users to upload an image and use a brush to mark the areas they want to restore. The application provides two inpainting algorithms - Telea and NS (Navier-Stokes). Users can select the algorithm and view the inpainted results in real-time.

## What is Image Inpainting?
Image inpainting is a class of algorithms in computer vision where the objective is to fill regions inside an image or a video in a way that it fits the context of its surroundings.

The region is identified using a binary mask, and the filling is usually done by propagating information from the boundary of the region that needs to be filled.

A common application of image inpainting is the restoration of old scanned photos. It is also used for removing small unwanted objects in an image.
## Image impainting algorithms : 
### Navier-Stokes & Fast Marching
INPAINT_NS : Navier-Stokes based Inpainting
This method was published in 2001 in a paper titled "Navier-Stokes, Fluid Dynamics, and Image and Video Inpainting".

This paper shows off how the field of Computer Vision is a melting pot of different disciplines, pulling concepts from fields like electrical engineering, computer science, physics, and mathematics. They bring their ideas to the field and solve the same problem in very interesting and unique ways. An electrical engineer may see an image as a 2D signal and apply the theories of signal processing to solve computer vision problems. On the other hand, a mathematician may see an image as a connected graph and solve computer vision problems using graph theory.

So it isn’t surprising that theories developed for fluid dynamics also make their way into computer vision.

### INPAINT_TELEA : Fast Marching Method based
This implementation is based on a paper titled "An Image Inpainting Technique Based on the Fast Marching Method" by Alexandru Telea.

This implementation solves the same constraints using a different technique. Instead of using the image Laplacian as the estimator of smoothness, the author uses a weighted average over a known image neighborhood of the pixel to inpaint. The known neighborhood pixels and gradients are used to estimate the color of the pixel to be inpainted.

Once a pixel is inpainted, the boundary needs to be updated. The author treats the missing region of the image as level sets and uses the fast marching method to update the boundary.

## How to Use
### Installation:

Clone this repository to your local machine.

### Setup Environment:

It's recommended to create a virtual environment to manage the dependencies for this project.
Navigate to the project directory and create a virtual environment: python -m venv venv
### Activate the virtual environment:
#### On Windows:
venv\Scripts\activate
#### On macOS and Linux:
source venv/bin/activate

### Run the Application:

#### Execute the Streamlit application:

streamlit run 10_03_image_inpaint_streamlit.py

This will open a new tab in your web browser with the Image Inpainting application.

## Image Inpainting:

Upload an image that you want to restore using the "Upload Image to restore" button.
Adjust the "Stroke width" slider to set the size of the brush strokes.
Draw over the damaged or missing areas of the image using the brush provided on the canvas.
Choose the inpainting algorithm from the "Mode" dropdown - Telea, NS, or both for comparison.
The inpainted result will be displayed in real-time based on your selection.
You can also choose to show the mask you created by checking the "show mask" checkbox.
Download Output:

After using the inpainting algorithm, you can download the inpainted image by clicking the "Download Output" link provided in the sidebar.
## About
This application is a demo for image inpainting using Streamlit, OpenCV, and other Python libraries. It was created by [Nasser] 
Feedback and Contributions
If you have any feedback, suggestions, or would like to contribute to this project, please feel free to open an issue or submit a pull request. Your contributions are greatly appreciated!

## Credits
This project uses the following libraries:

Streamlit
OpenCV

