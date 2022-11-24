The Python program for automatic interpretation of color patches was developed to facilitate the spatial color pattern calculation. The procedure steps and how them works were explained as follows.
Step 0: Image Prepossessing.
The perturbed colors in the images are replaced by the colors never appeared in all photographs by Adobe Photoshop manually. The processed images are the inputs to the programs of automatic interpreting color patches. In Figure B1, the photograph (a) was original, and photograph (b) was the processed one.

In programming, the original photograph was treated as a three-dimensional matrix of 6000 × 4000 × 3, where 6000 × 4000 is the width and height of the photo, and 3 represents the values of RGB of pixels. Therefore, an original photograph was represented as an orderly combination of 6000 × 4000 × 3 numbers.

Step 1: Image Compression. To improve the processing speed, we resample and compress the photograph using pixel area relation with resolution of 600 × 400 × 3, which could reduce the processing time by 100 times.

Step 2: Color Space Conversion. The color space of photograph was converted from RGB to HSV based on the algorithm below.
        
Step 3: Compress the Color Space. Each pixel in the photograph is compressed into 256 colors from full color (16,777,216 colors) based on the algorithm below.
       
Step 4: Further Compression of the Color Space. Replace the color of every pixel with the highest ratio color in the classification which were listed in Table A1. The photograph was compressed into 25 colors from 256 colors. In Figure B2, photograph (a) has 256 colors and photograph (b) has 25 colors, and some details especially the dark part of the photo was optimized.

Step 5: Gaussian Blur. To lower the impact of noises on color patch division, Gaussian Blur Algorithm is used to smooth the photos. The step size of blurring used in the paper was 8 × 8, and it should be adjusted according to contents and resolutions of photos.

Processed from Step 0 to Step 5, the color patches in the photographs have been basically interpreted as shown in Figure B3.

Step 6: Generate IDF_ASCII Files. Fragstat was used to calculate the metrics of color patches patterns. The photograph was not supported as the input files, and it should be converted to the files in IDF_ASCII format. In this step, every pixel was replaced by the number of its color category, and a two-dimensional matrix of 600 x 400 numbers was generated.

Step 7: Calculate the Metrics. The landscape scale was selected in the Fragstat, and the values of metrics of color patterns were calculated.

Step 8: Repeat from Step 0 to Step 7 until all the photographs were processed. And the metrics were calculated photograph by photograph.

Citation:   Cao, Y.; Li, Y.; Li, X.; Wang, X.; Dai, Z.; Duan, M.; Xu, R.; Zhao, S.; Liu, X.; Li, J.; et al. Relationships Between the Visual Quality and Color Patterns: Study in Peri-Urban Forests Dominated by Cotinus coggygria var. cinerea Engl. 
in Autumn in Beijing, China. Forests 2022, 13, x. 
