# Image-Processing

Implement the basic image processing methods: convolution/correlation, template matching, color histogram analysis, Canny edge detection.

**1D Convolution**

After loading the staircaase image included with scipy.misc

  * Calculate the height and width of the staircase image and display the image
  * Retrieve the first row of the image
  * Create a numpy array with the finite difference filter [-1, 1]
  * Apply the filter to one row of the image (no need to reverse it for convolution). Please implement this yourself only using NumPy functions but not OpenCV or scipy
  * Plot the intensity of the first row and the output of the finite difference filter on a graph (the x value should be the index and the y value the intensity)

**2D Linear Filters**
  * Create 3x3 numpy arrays for the linear filter to highlight vertical edges and horizontal edges (consult Lecture 5)
  * Apply signal.convolve2d (see reference guide https://docs.scipy.org/doc/scipy/reference/generated/scipy.signal.convolve2d.html (Links to an external site.))
  * Display the original image and the 2 filtered images

**OpenCV Template Matching**

Evaluate the performance of 2 OpenCV template matching options (cv2.TM_COEFF and TM_CCORR) at finding Waldo. You are allowed to use any OpenCV methods that you wish. https://docs.opencv.org/master/d4/dc6/tutorial_py_template_matching.html (Links to an external site.)

  * Load and display the puzzle image and the query image. Calculate the height and the width of the query image (Waldo).
  * Apply the template matching method and display the result.
  * Find the location of the max value in the result.
  * Make a copy of the puzzle image using copy() and draw a rectangle on the maximum location. To size the rectangle, use the height and width of the Waldo query image. (the reason you are making a copy is to avoid drawing rectangles from both the methods on the same image).
  * Display the image with the rectangle drawn.
  * Repeat the procedure using the other method
  * Report which method correctly finds Waldo.

**Color Histograms**

  * Load the images of the parrot, group of parrots and the vacuum cleaner.
  * Display the images.
  * Calculate the color histogram of the images and normalize them. Please consult the OpenCV documentation for this: https://docs.opencv.org/3.4/d8/dbc/tutorial_histogram_calculation.html (Links to an external site.) Remember that by default openCV loads images using BGR convention.
  * Plot the color histograms for the blue, green, and red values (preferably on the same axes using a bin size of 256)). Do this for each of the three images.
  * Recalculate the histograms using bin sizes of [8, 8, 8] for b,g,r and compare them using compareHist cv2.HISTCMP_INTERSECT (intersection). Print the results of comparing the parrot image to itself, to the group of parrots and to the vacuum cleaner.

**Canny Edge Detection**

  * Convert the parrot image to grayscale
  * Apply the Canny edge detection OpenCV function it with low threshold of 100 and high threshold of 200.
  * Display the result.
