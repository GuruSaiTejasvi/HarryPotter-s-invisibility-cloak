# HarryPotter-s-invisibility-cloak
This project implements a simple "Invisible Cloak" effect using Python and the OpenCV library. The idea is to create an illusion that a person wearing a specific color (in this case, red) appears as if they are wearing an invisible cloak. The project uses color detection and image processing techniques to achieve this effect.

Here's a step-by-step explanation of the code:
1. Importing libraries:
   The necessary libraries are imported. numpy is used for numerical operations, and cv2 (OpenCV) is used for computer vision tasks.
   
2. Initializing the camera:
   A VideoCapture object is created to capture video from the default camera (index 0).
   
3. Capturing the background:
   The program waits for 2 seconds to allow the camera to adjust, and then it captures the background frame by reading the video feed 50 times. This is done to obtain a stable background without the person in it.

4. Main loop:
   A continuous loop is established to read frames from the camera.

5. Color detection and masking:
   The frame is converted to the HSV color space, and a mask is created to isolate the red color. The mask is a binary image where pixels within the specified red color range are set to 1, and others are set to 0.

6. Morphological operations:
   Morphological operations (opening and dilation) are applied to the mask to smooth it and fill gaps. Another mask (mask2) is created as the inverse of mask1.

7. Image blending:
   The background is extracted using mask1, and the person is extracted using mask2. The two images are then blended together using the addWeighted function.

8. The resulting frame with the "Invisible Cloak" effect is displayed. The program exits when the 'Esc' key is pressed. Finally, the camera is released, and all OpenCV windows are destroyed.

This project is a fun example of using computer vision techniques to create a visually interesting effect.

I have developed this project when I am part of the Computer Science and Engineering Association at NIT ANDHRA PRADESH, as a part of OpenCV projects EXPO.
