1. Suppose you want to detect edges at a 2x reduced spatial scale. You have two choices: double the size of your gradient filters, or halve the size of your image. Calculate and compare the number of multiplications required per input pixel to perform each of these approaches. Assume that your downsampling prefilter is 5x5 and a “double size” sobel filter would be 7x7 (i.e., the half-width is doubled). Which approach will be more efficient if you want to detect edges at multiple reduced spatial scales?

It would be computationally more effcient to down size first and then run the 5x5 filter. 

2. Suppose you have a 128x128 image, and you compute a full Gaussian pyramid. How much storage (measured in pixels) is required to store the whole Gaussian pyramid? Also compute the square root of your answer to show the dimensions of a single square image requiring the same amount of storage as the pyramid of the 128x128 image.

(128^2)+(64^2)+(32^2)+(32^2)+(16^2)+(8^2)+(4^2)+(2^2)+(1^2)=22869

3. Suppose you are given the Laplacian and Gaussian pyramids for an input image I.
 G0…k are the Gaussian pyramid levels starting at the original image (G0), while the Laplacian layers L0…k are the “detail” layers, with each Li at the same resolution as Gi. When is it the case that Gℓ=Lℓ?

These transformations will have the same resolutions on thier first layer. As the Gausian downsamples on each layer and the laplacian uses a band pass.

Chat GPT: " When does Laplacian and Gaussian pyramids for an input image have the same resolution?"

4. Given all levels of both pyramids, give an expression that yields a result as close as possible to Gj with a sharpening filter applied. You don’t need to actually do any filtering.

I do not recall well.


5. Give an algorithm to reconstruct G0 using only the levels of L.



