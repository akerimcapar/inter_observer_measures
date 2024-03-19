
# An Interpretable Framework for Inter-Observer Agreement Measurement in TILs Scoring on Histopathologic Breast Images

## Abstract
Breast cancer poses significant global health challenges, emphasizing the need for precise diag-nostic tools. Tumor-Infiltrating Lymphocytes (TILs) play a crucial role in understanding the immune response to breast cancer. Despite their significance, existing inter-observer variability in TILs scoring methods hampers reliable assessments. This study introduces an innovative and in-terpretable framework to address this challenge. The proposed framework comprises two novel inter-observer agreement measures: Boundary-Weighted Fleiss’ Kappa (BWFK) and Distance-Based Cell Agreement Algorithm (DBCAA). These measures offer adaptability for assessing the concordance of artificial intelligence methods with pathologists. Thoroughly validated on a clinical dataset, the framework contributes to standardized, reliable, and interpretable in-ter-observer agreement assessments, addressing the critical need for consistency in breast cancer pathology. The study underscores the potential impact of these measures in advancing histo-pathologic image analysis, fostering consensus in TILs scoring, and ultimately improving breast cancer diagnostics and treatment planning.

## Graphical Abstract
![Graphical Abstract](images/Gaphical_Abstract.png)

## Implementation Guide

### 1) Prepare input images
Prepare the histopathological images to measure the inter-observer agreements. Images can be obtained by capturing from microscopes or cutting patches from whole slide images.

<img src="images/input_images.png" width="500">

### 2) Annotations
Use a platform such as Roboflow (https://roboflow.com), LabelMe (http://labelme.csail.mit.edu/Release3.0), LabelBox (https://labelbox.com) or use another commercial software to obtain the annotations of observers. Besides, you can run your AI methods on the input images to get AI based annotations. 
* Regional Annotations: Create binary mask images to remark the annotated stromal regions for each input image and each observer. Mask images must be the same size as input images. Sample mask images are given in sample_data folder.
<img src="images/sample_image_mask.png" width="500">

* Cell Annotations: Cells are marked with boundary boxes by observers. Cell boundary boxes are stored as ASAP xml file format (https://github.com/computationalpathologygroup/ASAP). Sample cell coordonate xml files are given in sample_data folder.
<img src="images/ASAP_xml.png" width="700">

### 3) Prepare data folders
Data folder is prepared to run the agreement measures. Structure of the folder should has the following format:
```
DATA_DIRECTORY/
├── image1/
    ├── observer1/
      ├── mask.png
      ├── lymphocyte.xml  
    ├── observer2/
      ├── mask.png
      ├── lymphocyte.xml  
    └── ...
├── image2/
    ├── observer1/
      ├── mask.png
      ├── lymphocyte.xml  
    ├── observer2/
      ├── mask.png
      ├── lymphocyte.xml  
    └── ...
└── ...
```
A sample folder is given in sample_data folder.
### 4) Run measurements
Run the codes to calculate inter-observer agreement measurements for the sample data folder.
* BWFK: Run the code given in BWFK.py to calculate stromal inter-observer agreement values.
* DBCAA: Run the code given in DBCAA.py to calculate lymphocyte detection inter-observer agreement values.
* TILS ICC: Run the code given in TILs_ICC.py.py to calculate the TILs scores and ICC inter-observer agreement values.

### 5) Interpret results
The results obtained by following this guide can be used for different purposes.
* AI methods can be validated using the guide. Results of an AI method can be processed as an observer and can be compared with the results of phycisian observers to validate the performance of the method
* The guide can be employed  for pathologist trainings to improve the inter-observer concordance on TILs scoring. Stromal segmentation, lymphocyte detection and overall TILs scoring based agreements can be obtained and can be examined statistically to find the source of the TILs scoring based inter-observer variabilities.



