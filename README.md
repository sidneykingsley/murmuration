# Introduction
This is the source code to run my pix2pix-tensorflow trained model.
The model has been trained on a dataset of 1000 images taken from the recorded visual output of i-DAT's *Murmuration* project, one of the outcomes from their collaboration with the European Mobile Dome Lab. When installed Murmuration responded to its audience 'through playful interaction with particle swarms of digital detritus and real-time manipulation of virtual/physical audio-visual objects' (Kissick, 2016). In my machine learning interpretation of this project I hoped to achieve a similar effect.
My model has been trained using pix2pix. Pix2pix uses conditional adversarial networks to achieve image-to-image translation, it can be used in a variety of ways but in my project,  it is used to solve 'Edges to Photo'. 


# Documentation
A video document of my model responding to live video input can be seen at **//VIMEO LINK HERE//**
Image documentation can be found in the 'screen-captures' section of this repository.
Examples of the model making guesses from its 'A' source data can be found at **//TEST INDEX.HTML LINK HERE//**


# Code
The code used in this project can be divided into three sections:
1. Dataset gathering and processing (https://github.com/sidneykingsley/edge-detection)
2. Training of the model (https://github.com/sidneykingsley/pix2pix-tensorflow)
3. Visualisation (https://github.com/sidneykingsley/murmuration)


# Running the Project
1. To run this project please first clone the GitHub repository: https://github.com/sidneykingsley/murmuration
2. Secondly, please set up a virtual python environment running Python 3.6.5 and install the required dependencies:
- OpenCV 3.0+ (I used 4.0.0)
- Tensorflow 1.4.1
- PyQt
- PyQtGraph (0.10)
3. Download my model from **//ADD LINK HERE//**
4. Place the downloaded folder within the 'models' directory
5. Run 'python webcam-pix2pix.py' from your virtual env.


# Adjustments
If I were to continue with this project, I would make some adjustments to the dataset before re-training the model:
- I would run a batch process using a photo editing program like Adobe Photoshop or ImageMagick to increase the saturation and brightness of the images to create a more diverse visual response.
- Use a program such as ImageMagick to take multiple crops from each original image when resizing to 256px. The source content I used for my training was the sped-up output from the installation of the i-DAT Murmuration project provided by Professor Mike Phillips. As it was displayed on a large immersive dome the video output was of a high quality but also warped; this meant it would have been possible to take a few well positioned images from each frame rather than just one centrally cropped image.
- I also would have made adjustments to the python OpenCV edge detection program I wrote to generate outlined replications of my training data to use as the A input in my AtoB model: I believe the aesthetic effect could have been improved through lowering the sensitivity of the canny edge detector to reduce noise.
I would also have made adjustments or changed the GUI being used to simplify the visual output and pre-set the args with the ideal balance of pre-blur and pre-median for the edge detection processing. 
This project would be best executed on a machine with a powerful dedicated GPU. 



# Acknowledgements
- Memo Akten for his webcam-pix2pix-tensorflow pretrained model visualiser project (https://github.com/memo/webcam-pix2pix-tensorflow)
- Phillip Isola et al for pix2pix (https://phillipi.github.io/pix2pix)
- Christopher Hesse (@affinelayer) for his pix2pix-tensorflow port (https://github.com/affinelayer/pix2pix-tensorflow)
