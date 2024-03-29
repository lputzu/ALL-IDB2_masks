# ALL-IDB2_masks

Here, you can find some manually segmented masks for ALL-IDB2 data set images, provided by an expert pathologist. <br>
Each mask contains 3 labels, one for each image component as follows:<br>
<br>
background = 255, 255, 255<br>
nucleus = 0, 255, 255<br>
cytoplasm = 0, 0, 255<br>
<br>
For example to extract the mask for the whole cell:<br>
<br>
In Python<br>
background = cv2.inRange(img, np.array([255,255,255], dtype=np.uint8), np.array([255,255,255], dtype=np.uint8))<br>
#to obtain the cell mask<br>
mask = 255 - background<br>
<br>
In MATLAB<br>
background = img(:,:,1)==255 & img(:,:,2)==255 & img(:,:,3)==255;<br>
#to obtain the cell mask<br>
mask = 1 - background<br>
<br>
Authors, releasers and maintainers: Andrea Loddo, Lorenzo Putzu - University of Cagliari

NOTE: please cite one of the following pubblication in case of using these images in your own work:

@article{CDR2016, author = {Cecilia Di Ruberto and Andrea Loddo and Lorenzo Putzu}, title = {A leucocytes count system from blood smear images - Segmentation and counting of white blood cells based on learning by sampling}, journal = {Mach. Vis. Appl.}, volume = {27}, number = {8}, pages = {1151--1160}, year = {2016}, url = {https://doi.org/10.1007/s00138-016-0812-4}, doi = {10.1007/s00138-016-0812-4} }


@Article{app12073269,
AUTHOR = {Loddo, Andrea and Putzu, Lorenzo},
TITLE = {On the Reliability of CNNs in Clinical Practice: A Computer-Aided Diagnosis System Case Study},
JOURNAL = {Applied Sciences},
VOLUME = {12},
YEAR = {2022},
NUMBER = {7},
ARTICLE-NUMBER = {3269},
URL = {https://www.mdpi.com/2076-3417/12/7/3269},
ISSN = {2076-3417},
DOI = {10.3390/app12073269}
}

@Article{ai2030025,
AUTHOR = {Loddo, Andrea and Putzu, Lorenzo},
TITLE = {On the Effectiveness of Leukocytes Classification Methods in a Real Application Scenario},
JOURNAL = {AI},
VOLUME = {2},
YEAR = {2021},
NUMBER = {3},
PAGES = {394--412},
URL = {https://www.mdpi.com/2673-2688/2/3/25},
ISSN = {2673-2688},
DOI = {10.3390/ai2030025}
}


Further segmented masks for ALL-IDB1 data set images can be found @ https://github.com/andrealoddo/ALL-IDB1-masks

# ALL-IDB
ALL-IDB is a public image dataset described in the following article: https://ieeexplore.ieee.org/document/6115881 More information can be found @ https://homes.di.unimi.it/scotti/all/

# LICENSE
MIT License

Copyright (c) 2021 Andrea Loddo, Lorenzo Putzu

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
