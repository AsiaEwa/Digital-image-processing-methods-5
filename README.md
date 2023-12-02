# Digital-image-processing-methods-5
## Digital image interpolation methods

A script using nearest neighbor interpolation
orginal picture:
![image](https://github.com/AsiaEwa/Digital-image-processing-methods-5/assets/101841759/dcf4450a-c1f3-4701-be3e-829df114c7b5)

X10:

![image](https://github.com/AsiaEwa/Digital-image-processing-methods-5/assets/101841759/f6bb8e36-2439-468b-b675-b0e1c5893810)

X.0.1:

![image](https://github.com/AsiaEwa/Digital-image-processing-methods-5/assets/101841759/00362aa0-3f4d-4371-910f-9a60775d8af6)

The nearest neighbor method uses the least memory because it requires the least amount of computation and only works in one direction. (photo less clear). The bicubic interpolation method consumes the most memory because it requires the largest number of calculations in the largest number of directions.

Image shrinking is performed for parameter M from 0 to 1 excluding 0 and 1, because 0 cannot be used because it is impossible to create an image smaller than 1x1 pixel, and 1 gives us the unchanged image size.
For the M parameter from 1 to a value depending on the input image. It is performed so as not to exceed the maximum dimensions of the array, for this function it is 1000000x1000000, the rand function works for such dimensions.

Using the bilinear interpolation function, an image with a given number of columns and rows was generated.

a) the proportions of the Lrows/Lcolumns are preserved as in the original painting,

![image](https://github.com/AsiaEwa/Digital-image-processing-methods-5/assets/101841759/fcb8b65b-944a-408a-9ba1-8c98f1977c42)

b) other than original proportions. (noticeable visual widening-stretching)

![image](https://github.com/AsiaEwa/Digital-image-processing-methods-5/assets/101841759/51b23106-9a55-48e6-8553-6e3a603cf931)

For modification:

a) the generated image has been reduced twice in size and there is no noticeable deterioration in quality in any of the image directions. Checking the internal parameters, it can be concluded that the resolution has decreased twice in each direction.

b) the image was reduced twice vertically, but retained its original size horizontally. There is no deterioration in quality, but there is horizontal distortion and unnatural "stretching".

magnification x2 using nearest neighbor and then x4 using bicubic interpolation

Comparison of results with x6 magnified image using bicubic interpolation.

x2 magnification – nearest neighbor method

![image](https://github.com/AsiaEwa/Digital-image-processing-methods-5/assets/101841759/7e17e9f7-bbfb-4dce-95e8-0aab837a06f0)

x4 magnification – bilinear interpolation method

![image](https://github.com/AsiaEwa/Digital-image-processing-methods-5/assets/101841759/bec0e72b-de03-4915-907a-d02cca406d79)

x6 magnification – bicubic interpolation method

![image](https://github.com/AsiaEwa/Digital-image-processing-methods-5/assets/101841759/8772e395-3300-430c-92cb-00e17b88efed)

Image comparisons: using methods:

• nearest neighbor - bicubic interpolation
You may notice the poorer quality of the twice-magnified image. It shows non-linearity of the edges of image elements and the effect of "jagged" edges compared to an image enlarged six times. Despite this, the image enlarged twice beyond the edges seems slightly sharper.

• bilinear interpolation - bicubic interpolation
An image enlarged four times is of lower quality. You can see that it is more blurry compared to the image enlarged six times.
