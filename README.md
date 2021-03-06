# architecture-style-recognizer

Using pre-trained CNNs to recognize different (mostly western) styles of (exterior) architecture. Images scraped from [images.google.com](images.google.com). Code outline from [fast.ai's MOOC](https://course.fast.ai/). 

Validation Set Accuracy (%)   | Date Obtained (MM/DD/YY) | Model       | Number of Classes\* | Examples Per Class (on avg.) Before Data Cleaning
|-----------------------------|--------------------------|-------------|---------------------|--------------------------------------------------
| 75.4			      | 01/05/20		 | DenseNet121 | 9	 	     | 200
| 71.4                        | 01/04/20                 | ResNet50    | 9                   | 200
| 68.3                        | 01/03/20                 | ResNet34    | 9                   | 200
| 72.1\*\*                    | 01/02/20                 | ResNet34    | 10	             | 400
| 65.0                        | 01/01/20                 | ResNet34    | 10                  | 200

\*I removed the Bauhaus style after realizing that a large number of Google images of "bauhaus architecture exterior" were of the same buildings. It also seemed to be not dissimilar enough from modernist architecture from sources online that seemed to have domain expertise.

\*\*This result is unfortunately quite difficult to reproduce as I was not consistent in manually cleaning the data (I underestimated the mass that is 4000 images).

# other work

[Mathias et. al 2012](https://www.researchgate.net/publication/273685892_Automatic_architectural_style_recognition) uses classical computer vision and segmentation techniques on _three_ classes of architectural styles and obtains an accuracy of 84%, suggesting that deep learning may be a good approach for this problem.
