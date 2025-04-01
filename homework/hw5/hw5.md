1. In terms of uniqueness and invariance, discuss why single pixels, described using their RGB values, do not make good features for image matching.

There can be several pixels in an image that are the exact same color, therefore you cannot differentiate where in the image you are. 

2. For each of the following (linearized) error function shapes, describe the image patch that gave rise to it:
    1. Flat in all directions: Single color or hue
    2. Steep in one direction, flat in the orthogonal direction: changes color or hue along one axis such as a line
    3. Steep in all directions: has lot of different color and hue very high frequentcy.


6.Why did our code pick them up, and what would we need to change in order to get only things that really do look like corners in the image?

(I am in a bit of time crunch given that my take home exam for another class got moved back a day) However, I believe that our code could only work in picking up features in the x direction, which would not detect image variance in the y-axis. 


