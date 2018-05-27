# Project: Finding Lane Lines on the Road
My aim was to make a code which could identify the lane lines on the road from the picture provided

## Reflections of the project
1) FIrst I converted my image to grayscale image. This was followed by applying Gaussian Filter so as the image becomes smooth. **

2) After this my aim was to detect all the edges in the image. For this i called Canny() function.

3) Now my aim is to select specific region where i expect the lane lines to be. This was done with the help of functions like fillPoly().

4) Now since i have all the edges with me, i need to identify the lane lines using the Hough transformation method. This required calling HoughLinesP() function.

5) With this most of the issues were resolved but still there were some areas were i couldn't fine the lane lines from start. For this i took all the x and y coordinates which I got from HoughLinesP() of the formed line and on the basis of that I calculated m and c (for line y = mx + c). With the help of this i drew the lines from start.

## Shortcomings with the current pipeline
1) Roads having Curved lane lines cannot be detected by this code as we are assuming the lane lines on straight line and hence this cannot be applied to the Curved lanes

2) It is also not possible to detect the lane lines where we have too much of noise. Lane lines under shadow of tree is one such example

## Possible improvements in current pipeline
1) There should have been some algorithm for Curve as well instead of just line detection

2) Algorithm which can detect lane lines even when there is too much noice should have been used
