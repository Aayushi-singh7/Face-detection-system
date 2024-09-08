# Face-detection-system
Created using OpenCV  , deepFace libraries in python
CODE EXPLANATION:

In our face recognition project, we use various face detection & recognition algorithms to verify if the facial features match with the reference image.
The code is written in python using python libraries like OpenCv , threading and deepface using tensorflow.
Upon matching the image it shows :
Match! 
If the face detected did not match then it shows:
No Match! 
A recurring while loop is used to continuously detect the faces in the frame and recognize if it matches with the given reference.jpg.
The loop face detection program can be ended by pressing “q” in the keyboard.

CODE STEP-by-STEP EXPLANATION:
This code is a Python script that uses OpenCV and the DeepFace library to perform real-time face verification using a webcam. It continuously captures frames from the webcam, checks for face matches with a reference image, and displays the results on the video feed.

Here's a breakdown of the code:

Import Libraries:

threading: Used for creating a separate thread to handle face verification asynchronously.
cv2: OpenCV for video capturing and image processing.
DeepFace: A deep learning-based face recognition library.
Initialize Video Capture:

Open a connection to the default camera (index 0) using cv2.VideoCapture(0, cv2.CAP_DSHOW).
Set the frame width and height to 640x480.
Global Variables:

counter: A counter to control the frequency of face verification checks.
face_match: A boolean flag to indicate whether a face match is detected.
reference_img: Load the reference image for face verification.
check_face Function:

A function that performs face verification using DeepFace.
It checks if the provided frame matches the reference image using DeepFace.verify().
If a match is found, it sets face_match to True, otherwise, it sets it to False.
Handles the case where a ValueError occurs during the verification.
Main Loop:

Continuously captures frames from the webcam using cap.read() in a while True loop.
Every 30 frames (adjustable with counter % 30), it launches a new thread to perform face verification using the check_face function.
Displays the result on the video feed using cv2.putText based on the value of face_match.
The video feed is displayed using cv2.imshow.
The loop breaks if the user presses the 'q' key.
Cleanup:

Closes all OpenCV windows when the script is terminated.
Note:

The script uses threading to perform face verification asynchronously, allowing the main loop to continue capturing frames without waiting for the verification process to complete.
The DeepFace.verify function is employed for face verification, comparing the current frame with the reference image.
The ValueError handling in the check_face function ensures that the program doesn't crash if an error occurs during face verification.
Make sure you have the necessary libraries installed (cv2 and deepface) before running the script. Additionally, ensure that the reference.jpg file contains a valid reference face image for comparison.



                                                            DATASETS AND THEIR LINKS


What is a Face Recognition Dataset?
                                                                                                                                                         Most people can recognize about 5,000 faces, and it takes a human 0.2 seconds to recognize a specific one. We also interpret facial expressions and detect emotions automatically. In other words, we’re naturally good at facial recognition and analysis. But, in recent years, Computer Vision (CV) has been catching up and in some cases outperforming humans in facial recognition. Advances in CV and Machine Learning have created solutions that can handle tasks more efficiently and accurately than humans. The applications of this technology are wide-ranging and exciting. One example is in marketing and retail. Saks Fifth Avenue uses facial recognition technology in their stores both to check against criminal databases and prevent theft, but also to identify which displays attract attention and to analyze in-store traffic patterns. Powering all these advances are numerous large datasets of faces, with different features and focuses. Sifting through the datasets to find the best fit for a given project can take time and effort. 
A quick guide to some popular and high-quality, public datasets focused on human faces.:
 
 
Digi-Face 1M
•	Released – 2022 
•	Description – Digi-Face 1M is the largest scale synthetic dataset for face recognition that is free from privacy violations and lack of consent.
•	Face Images  – 1.2 million
•	Identities – 110,000
•	Licensing – The Digi-Face 1M dataset is available for non-commercial research purposes only.
•	Download the dataset here.: https://github.com/microsoft/DigiFace1M
CelebFaces Attributes Dataset (CelebA)
•	Released – 2015 
•	Description – CelebFaces Attributes Dataset (CelebA) is a large-scale face attributes dataset with more than 200K celebrity images, each with 40 attribute annotations. The images in this dataset cover large pose variations and background clutter. 
•	Face Images  – 202,599
•	Identities – 10,177
•	Licensing – The CelebA dataset is available for non-commercial research purposes only.

