<h2>Lane Detection using OpenCV</h2>
<p>The following code uses OpenCV library to detect lane markings on the road. It reads a video file and outputs another video file with the detected lanes overlayed on the original video.</p>
<h3>Required Libraries</h3>
<ul>
    <li>OpenCV</li>
    <li>numpy</li>
</ul>
<h3>Functions</h3>
<ul>
    <li><code>make_points(image, line)</code>: Returns the endpoints of a line on the image based on its slope and y-intercept.</li>
    <li><code>average_slope_intercept(image, lines)</code>: Returns the averaged lines on the left and right lanes based on the slopes and y-intercepts of the detected lines.</li>
    <li><code>canny(img)</code>: Returns the canny edge detection of the input image.</li>
    <li><code>display_lines(img,lines)</code>: Returns the input image with the detected lines overlayed on it.</li>
    <li><code>region_of_interest(canny)</code>: Returns the masked canny image based on the region of interest specified as a triangle.</li>
</ul>
<h3>Main Code</h3>
<p>The main code reads a video file named &quot;test2.mp4&quot;. For each frame in the video, it does the following:</p>
<ul>
    <li>Applies canny edge detection.</li>
    <li>Masks the canny image based on the region of interest.</li>
    <li>Detects the lines on the masked canny image using the HoughLinesP transform.</li>
    <li>Averages the detected lines on the left and right lanes.</li>
    <li>Overlays the averaged lines on the original frame.</li>
    <li>Writes the resulting frame to a new video file named &quot;output.mp4&quot;.</li>
</ul>
