1. Comment on whether (or the extent to which) the Harris corner detector is robust to each of the following transformations. In other words, which of these will not affect which points will be found as corners by the Harris detector? If the detector is almost but not quite completely robust to a given change, comment on this. Assume edge effects and intensity clipping are not an issue.

    1. Intensity shift: $I(x, y)' = I(x, y) + 20$ robust
    2. Intensity scale: $I(x, y)' = 1.2 I(x, y)$ normailze the intenisity to make it robust
    3. Scaling: $I(x, y)' = I(0.5x, 0.5y)$ robust
    4. Translation $I(x, y)' = I(x - 10, y)$ robust
    5. Rotation robust

For each transformation pictured below, find a 2x2 transformation matrix that maps the original (left) image’s coordinates to the corresponding point in the right image. In all cases, the right image’s (0, 0) point is at the bottom left corner of the image (bottom corner of the image, in the case of #4.) Also in all images, x
 points right and y
 points up.

2. 
  $$
  \begin{bmatrix}
  1.3 & 0 \\
  0 & 1.3 \\
  \end{bmatrix}
  $$

3.

  $$
  \begin{bmatrix}
  2.0 & 0 \\
  0 & 1.0 \\
  \end{bmatrix}
  $$
4.

  $$
  \begin{bmatrix}
  1.0 & 0.5 \\
  0 & 1.0 \\
  \end{bmatrix}
  $$

  5.   
  
  $$
  \begin{bmatrix}
  cos(30) & sin(30) \\
  -sin(30) & cos(30) \\
  \end{bmatrix}
  $$

  6. 

$$
  \begin{bmatrix}
  1 & 0 & 40 \\
  0 & 1 & 40 \\
  0 & 0 & 1 \\
  \end{bmatrix}
  $$


  

  


