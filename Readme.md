
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
* Regional Annotations: Create binary mask images to remark the annotated stromal regions for each input image and each observer. Mask images must be the same size as input images. 
<img src="images/sample_image_mask.png" width="500">

* Cell Annotations: 

### 3) Prepare data folders
sadfsdafsadf

### 4) Run measurements
sadfsdafsadf

### 5) Interpret results
sadfsdafsadf


```
asdasdasd
```
