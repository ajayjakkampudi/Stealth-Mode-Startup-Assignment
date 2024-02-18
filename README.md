## **Finding Total Number of Dribbles**

### Using Masking Technique for color of Ball (Yellow)
1. Converting every from BGR to HSV color space.
2. Defines range of HSV values for the yellow color.
3. Creates a binary mask for the yellow color.
4. Apply the mask to evey video frame
5. Converts the result to grayscale.
6. Finds contours in the masked frame.
7. Displays the masked image in grayscale and prints the coordinates of the contours.
8. After getting the mask extract the non-zero indices.
Acquire the mid-point of the starting pixel of the contour and the ending pixel of the contour. The midpoint will be the center of the contour.
9. We track the mid-point of the coordinate of acquired contour. 
10. Let intialize dribble_count = 1 

    If ball direction suddenly changes from down to up then dribble_count = dribble_count + 1.
    By following this method we can get the total number of dribbles. Total Number dribbles according to the code is 128.

### Using Hough Circle
1. Read the Video frame by frame.
2. Preprocess the Image : Convert frame into gray scale and blur the frame( to avoid the noise).
3. Apply Hough Circle Transform. Acquire the centers of the circle in each frame and track the center to count the dribbles. Follow the below process to find the dribbles count.
4. Let intialize dribble_count = 1 

    If ball direction suddenly changes from down to up then dribble_count = dribble_count + 1.
    By following this method we can get the total number of dribbles. Total Number dribbles according to the code is 128.

5. But this process is not feasible because Hough circle failed to identify ball in some frames.