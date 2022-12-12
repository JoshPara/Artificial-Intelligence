# Artificial-Intelligence
Final Project - License Plate Detection

**User Documentation - For Use and Understanding** 

https://www.youtube.com/watch?v=mkHGGgF2M1A - This is a link to the YouTube video demonstration of our project


About:
This is the final project for Introduction to Artificial Intelligence (6660-01) Fall Semester 2022. This project is designed as a license plate detection and recognition reader using computer vision. 


Python Requirements:
* Python version 3.6 (although this version of Python isn't the most recent version, this was the version we have been using in class all semester so we continued use of it in this project)
* For this project we used Pycharm community edition as our IDE since it has been the IDE we have personally been using all semester


The following are packages we have installed in our python interpreter for this project specifically:
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
1. Ensure that the following libraries are installed and that they can be imported successfully: imutils, pytesseract, and cv2(opencv-contrib-python)
2. Download Tesseract OCR from the following link (https://github.com/UB-Mannheim/tesseract/wiki), run the installation wizard, and make sure you save the download location of tesseract.exe from the file (The path of tesseract will be used in the code to specify the location of the tesseract application)
3. Download the license plate pictures from this GitHub repository, save the 5 pictures in the same folder, and copy the path to that folder as well
4. Copy the code into a blank python file in an IDE
5. In line 14 - paste the path to where tesseract.exe is located on the machine (from step 2) ((make sure to change the black slashes to forward slashes "/" in the path or the IDE will throw errors)) 
6. In line 17 - If desired to change the name of the text file being created/outputted to, this can be done here
7. In line 49 - Paste the path to where the picture folder (downloaded from this repository) is located on the device. It is important to note that in the file path, after the location of the folder, put the name of the first image followed by {counter} and followed by the picture extension. This is imperative so that the program will loop through the pictures in the folder. An example of this is: "C:/User/example/downloads/car_images/image{counter}.PNG", in this example all the pictures located in the folder are named "image1", "image2", "image3", "image4", and "image5". This is done so that every time the program loops through, the counter is increased by 1 and so the next file path is pointing to the next image.
8. Once all these steps are followed, tesseract is installed, and the paths are changed in the code, the program is ready to run!
9. While the program is running, windows with the picture that is being interpreted at various steps will be displayed on the screen. The name of what step it is on will be at the top of the picture window. In order to move onto the next step in the program these picture windows will need to be closed after you are done viewing them each time. (This is caused by "cv2.waitKey(0)", this was implemented this was for demonstation purposes so that the image at different stages could be viewed slower during the first image processing but closed out at a faster rate for the other pictures to fit within the view length limiations).
10. Once each picture is complete the detected license plate number will be displayed in the runtime Python Terminal at the bottom of the IDE (for user convenience) as well as written to the text document that is created. The program will loop and repeat the same steps for the rest of the pictures.
11. Once all the pictures have been analyzed the program will complete and the text file containing all the license plate numbers (LicensePlates.txt) can be viewed to seen the final resutls (This text document will be located in the same folder as this python script exists on the machine since we figured it would be more convenient for external users than specifying a designated path for the text file). 


Additional Notes:
* If using a different picture of a license plate then the ones provided, make sure the picture is very high quality, make sure the picture is a PNG, and make sure the picture is a straight on view to the license plate so that the detection can be the most accurate
* If adding or subtracting pictures to the picture folder in hopes of running more pictures through the program, line 23 must be changed from '5' (since that is how many pictures we had in our picture folder for testing and demonstration) to whatever number of desired pictures located in the folder being run.
* After the program has run completely there will be an image saved in the same folder as the license plate text document, this image is the altered image from the last picture that was run through the program, before it was sent to the tesseract application.

Additional Knowledge:
* Pytesseract - This serves as a wrapper for the Tessaract Optical Character Recognition Application
* Imutils - This library provides useful functions for image altering
* Opencv-contrib-python - This library provides useful functions to help solve computer vision tasks
