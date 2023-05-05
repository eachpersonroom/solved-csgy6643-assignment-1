Download Link: https://assignmentchef.com/product/solved-csgy6643-assignment-1
<br>



<h1>A) Programming Questions</h1>

The purpose of this project is to get familiar with the coding environment for the rest of the course, reading/writing images, displaying images, and making graphs. You will implement histogram equalization.

<strong>Hint for implementation: </strong>You can assume an intensity range [0-255] and hardcode the size of the histogram to be 256. You can make sure you have an image of type uint8 with min 0 and max 255 with the python code:

<em># Convert the image to type uint8 and scale intensity values to the range 0-255 </em>

<em># *Note* numpy min/max flatten the 2D array, so you obtain the min/max of the entire image </em>im_uint8 = ((im – np.min(im)) * (1/(np.max(im) – np.min(im)) * 255)).astype(‘uint8’)










<h1>A1) Histogram Equalization</h1>

<strong> </strong>

Implement histogram equalization and apply to image <strong>crowd.png</strong>, which you will find uploaded on NYUClasses. You may use the programming environment of your choice. However, we recommended Matlab, Python, and C++, as these are languages we can best support. <u>You are encouraged to use libraries/built in</u> <u>functions to read/and write images and display figures and graphs, <strong>but the rest of the implementation must</strong></u><strong> <u>be your own</u></strong><u>.</u> That specifically includes creating an image histogram (probability density function), computing the corresponding cumulative distribution function (CDF), and the creation of a new contrast adjusted image.




Implement the following functions:




def create_pdf(im_in):

<em># Create normalized intensity histogram from an input image</em>       return pdf




def create_cdf(pdf):

<em># Create the cumulative distribution function from an input pdf</em>       return cdf




def histogram_equalization(im_in):

pdf = create_pdf(im_in) <em># Your previously implemented function</em>      cdf = create_cdf(pdf) <em># Your previously implemented function</em>      <em># Create a histogram equalized image using your computed cdf</em>         return equalized_im




Write up a report including the following:




<ul>

 <li>Include a brief introduction and description of how histogram equalization works.</li>

</ul>




<ul>

 <li>Show <strong>png </strong>before and after histogram equalization, and the corresponding histograms (PDFs).</li>

</ul>




<ul>

 <li>Discuss how the image and histogram have changed, <u>and connect it back to your description in 1).</u></li>

</ul>




<ul>

 <li>Show the cumulative distribution function before and after histogram equalization <u>on the same figure.</u> <u>Describe what you see</u>. Explain the shape of each CDF and relate it back to image contrast and intensity histogram shape.</li>

</ul>




<ul>

 <li>Reapply the histogram equalization procedure on the corrected image. <u>Show and discuss the results</u>.</li>

</ul>




<ul>

 <li>Apply histogram equalization to another low contrast image (greyscale). <u>Show and discuss the results</u>.</li>

</ul>




<ul>

 <li>Histogram equalization is a global solution, modifying contrast with respect to the CDF of the <u>entire</u> <u>image</u>. Imagine you split the image into <u>smaller regions</u> (e.g. patches of 50×50 pixels) and apply <u>histogram equalization to each local patch independently</u>. <strong>In your own words</strong>, describe advantages and disadvantages of this strategy. <u>There are no right or wrong answers here</u>, the idea is to think critically about the method and answer honestly in your own words.</li>

</ul>




<ul>

 <li>Include all code as an appendix, i.e. copy and paste all your code at the end of your report.</li>

</ul>