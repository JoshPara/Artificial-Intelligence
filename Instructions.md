# Artificial-Intelligence
Final Project - License Plate Detection

**User Documentation - For Use and Understanding** 

https://www.youtube.com/watch?v=mkHGGgF2M1A - This is a link to the YouTube video demononstration of our project


About:
This project is for the final project for Introduction to Artificial Intelligence 6660-01 Fall Semester. This project is designed as a license plate detection and recognition reader using computer vision. 


Python Requirements:
* Python version 3.6 (although this version of Python isn't the newest version this was the version we have been using in class all semester so we continued use of it in this project)
* For this project we used Pycharm community edition as our IDE since it has been the IDE we have personally been using all semester


The following are packages we have installed in our Interpretor for this project:
* Cython - v0.29.32
* Pillow - v8.4.0
* imutils - v0.5.4
* numpy - v1.19.5
* opencv-contrib-python - v4.5.460
* pip - v21.3.1
* pytesseract - v0.3.8
* setuptools - v59.6.0
* wheel - v0.37.1


Instructions:
1. Ensure that the following libraries are installed and that they can be importanted successfully: imutils, pytesseract, and cv2(opencv-contrib-python)
3. Download Tesseract OCR from the following link (https://github.com/UB-Mannheim/tesseract/wiki), run the installation wizard, and make sure you save the download location of tesseract.exe from the file (The path of tesseract will be used in the code to specify the location of the tesseract application)
4. Download the license plate pictures folder from this GitHub repository and save the path to that folder as well
5. Copy the code into a blank python file in the IDE
6. In line 14 - paste the path to where tesseract.exe is located on the machine (from step 3) ((make sure to change the black slashes '\' to forward slashes '/' in the path or the IDE will throw errors)) 
7. In line 17 - If desired to change the name of the text file being created and outputted to, this can be done here
8. In line 49 - paste the path to where the picture folder (downloaded from this repository) is located on the device. It is important to note that in the file path, after the location of the folder to put the name of the first image followed by {counter} and followed by the picture extension. This is imperative to do so that the program will loop through the pictures in the folder. An example of this is: "C:/User/example/downloads/car_images/image{counter}.PNG", in this example all the pictures located in the folder are named "image1", "image2", "image3", "image4", and "image5". This is done so that every time the program loops through the counter is increased by 1 and so the new file path is pointing to the next image.
9. Once all these steps are followed, tesseract is installed, and the paths are changed in the code, the program is ready to run!
10. While the program is running windows with the picture that is being interpreted at varies steps will be displayed on the screen. The name of what step is on will be at the top of the picture window. In order to move onto the next step in the program these picture windows will need to be closed after you are done viewing them each time.
11. Once each picture is complete the detected license plate number will be displayed in the runtime Python Terminal at the bottom of the IDE as well as written to the text document that is being created. The program will then loop and repeat the same steps for the rest of the pictures.
12. Once all the pictures have been analyzed the program will complete and the text file containing all the license plate numbers (LicensePlates.txt) will be located in the same folder as this python script exists in on the machine. 


Additional Notes:
* If using a different picture of a license plate make sure the picture is very high quality, make sure the picture is a PNG, and make sure the picture is a straight on view to the license plate so that the detection can be the most accurate
* If adding or subtracting pictures to the picture folder in hopes of running more pictures through the program, line 23 must be changed from 5 (since that is how many pictures we have in our picture folder) to whatever number of pictures that are in the folder
* After the program has run completely there will be an image saved in the same folder as the license plate text document, this image is the altered image from the last picture that was run through the program before it was sent to the tesseract application.

Additional Knowledge:
* Pytesseract - This serves as a wrapper for the Tessaract Optical Character Recognition Applicaiton
* Imutils - This library provides useful functions for image altering
* Opencv-contrib-python - This libary provides useful functions to help solve computer vision tasks
