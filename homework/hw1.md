<ol type="1">
<li>Rank the following computer vision tasks from “low-level” to “high-level”. There is not necessarily a single right answer, but there are many orderings we should all be able to agree on.
<ol type="1">
<li>Smoothing out graininess in an image without blurring the edges of objects</li>
<li>For each pixel in a video frame, estimate the location of that pixel’s content in the following frame (i.e., estimate per-pixel motion vectors, AKA optical flow)</li>
<li>Labeling all the cats in a photo</li>
<li>Generating an English language explanation of why an image is funny</li>
<li>Brightening an image</li>
<li>Reconstructing the 3D geometry of an object given photos from multiple perspectives</li>
<li>Segmenting the foreground to create a background blur effect for videoconferencing</li>
</ol></li>

My answer as dicussed in class:

Lowest to highest<br>
5 - low level task just changing the threshhold<br> 
1 - adjusting a digital filter<br>
2 - This would be more challenging but with enough previous data and assuming it is fairly smooth video - this can be done with simple numerical methods. <br>
7 - Would require the computer to determine the foreground and background, which can be a challenge. <br>
3 - Labeling cats would require a higher order understanding of the entire image. <br>
6 This would require a higher order of the images and how they are oriented. There could even be missing prospectives that would further complicate this process. This reminds me of how newer cars have 3D surround cameras to show you your car in a third person 3D space.
<img src="https://di-uploads-pod16.dealerinspire.com/toyotaofnorthcharlotte/uploads/2024/05/backing-out-of-a-parking-spot-1024x576.png">
4 This is the highest level as the computer is not just attaching binary labels such as cat or not cat. But the computer has to understand the image wholistically and why it is funny or not funny. This also requires large langauge model. I just tested this with a Chat GPT prompt and it successfully idenifted why a Google "funny image" could be considered funny.
<img src ="hw1 p1.PNG">
<a href="https://www.google.com/search?sca_esv=18f6bc0f3068f17c&rlz=1C1GCEB_enUS1023US1026&sxsrf=AHTn8zqxnlyCP0r3KW_iVb_v7A-Rm56-Jg:1741728024997&q=funny+images&udm=2&fbs=ABzOT_CWdhQLP1FcmU5B0fn3xuWpA-dk4wpBWOGsoR7DG5zJBpcx8kZB4NRoUjdgt8WwoMs7jebc2P25mD9bLva5PWN4zVPkHTrJb1XtEJXPDPnM-3Nqyg2DpQYf0__rgvYp763OIecjzoIFfy78i14zuuq8VjKwTzdXysHa3ThpzB26XsMVr-le6W2GJjjK-ByWmchGvmx8IXZi5GRafB-atBi0COErXw&sa=X&sqi=2&ved=2ahUKEwiKuObB-oKMAxX1jYkEHelkNqQQtKgLegQIGBAB&biw=1707&bih=940&dpr=1.5#vhid=Ip3DjaEWgXLAdM&vssid=mosaic">Source to Googled Image</a>

<li><p>A (physical) pinhole camera is simply a box with a hole in it. Describe how the image would change if you made the distance from the pinhole to the back of the box longer or shorter. Assume the other box dimensions stay the same.</p></li>
<img src="hw1 p2.jpeg">
As the box's focal distance gets larger the camera captures a more narrow image. As the box gets smaller the camera captures a less narrow image.
<br>
<li><p>Given a 3-channel color image with width <code>width</code> and height <code>height</code> stored in a 3-dimensional array <code>F</code>, write pseudocode to give the image a reddish tint. Assume that <code>F[r, c, i]</code> is the syntax to access the value of the <code>i</code>th color channel (where 0 is red, 1 is green, 2 is blue) of the pixel at the <code>r</code>th row and <code>c</code>th column. Your answer can, but does not need to involve any color space transformations.</p></li>


```python
beans = imageio.imread("../data/beans.jpg") #load beans
beans = util.byte2float(beans) #normalize rgb values from 0-255 to 0.0-1.0
beans[:,:,0] = beans[:,:,0]*1.5 # beans is equal to beans with the red column multipled by 1.5 to make it more red
plt.imshow(beans.clip(0-1)) #show beans
```

*Sources*: Visited Dr. Wilson for asstistance in office hours. Used the chat gpt promopt: "how to make a code block in markdown" as I forgot



