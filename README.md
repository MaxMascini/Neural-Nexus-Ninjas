Neural-Nexus-Ninjas  
===
***MRI & Neuro Data Hackathon Stream II***  \
This repository encompasses a comprehensive pipeline for processing brain imaging data and leveraging machine learning to uncover relationships between brain tissue composition and age.

## Key Steps Used
1. ### Use Masks to Normalize Brain Data    
    Utilize masks to normalize brain data, ensuring consistent and meaningful analyses across participants.

2. ### Find Number of GM, WM, & CSF Pixels for Each Participant  
    Implement voxel brightness values to distinguish CSF (1), GM (2), and WM (3) in segmented brain images. Quantifying the presence of each tissue type for subsequent analysis.

3. ### Bin Labels/Ages
    Employ age binning to categorize ages into discrete groups, aiming for small bins conducive to effective classification. The resulting labeled dataset is then split into training and testing sets with a split of 0.2.

4. ### Feed into ML Classifier (Logistic Regression) and Label with Ages
    Leverage a Logistic Regression (LR) classifier to discern relationships between the amounts of GM, WM, & CSF and age. Seeking to achieve accurate age predictions based on brain tissue composition, providing insights into the intricate interplay between brain structure and aging.


# File Structure
## Get Brain Data

The `Get Brain Data.ipynb` notebook is responsible for obtaining the number of GM (Gray Matter), WM (White Matter), and CSF (Cerebrospinal Fluid) pixels from segmented images. 
The extracted data, along with participant metadata, is saved to a CSV file for later use in machine learning classification.

### Pathing Libraries and Image Libraries
The notebook uses several Python libraries for pathing and image manipulation, including `pathlib`, `os`, `nibabel`, `numpy`, `pandas`, `scipy.ndimage`, and `matplotlib.pyplot`.

### Pathing
Paths to the necessary data folders are defined, and a z-normalization function is provided to normalize image data using a binary mask.

### Find Pixels
The notebook iterates through participant data, loading segmented and mask data, and calculates the number of GM, WM, and CSF pixels for each participant. The results are then stored in a CSV file named `brain_data.csv`.

### Instructions
1. Open and run `Get Brain Data.ipynb` to generate the CSV file required for ML classification.

## ML Classification

The `ML Classification.ipynb` notebook utilizes the previously obtained GM, WM, and CSF pixel data to train a logistic regression classifier. The goal is to find relationships between brain tissue and age.

### Import Libraries & Pathing
The notebook imports necessary libraries for machine learning tasks, including `scikit-learn`, and sets up the pathing for data files.

### Preparing Data for Classification
Data is read in from the previously generated `brain_data.csv`. The age variable is binned, and a logistic regression classifier is trained to predict the age group based on GM, WM, and CSF pixels.
The trained-test split is 0.2 (0.8 trained, 0.2 tested).

### Machine Learning Classification
The notebook performs logistic regression classification, evaluates the model, and visualizes the results using metrics such as precision, recall, and a confusion matrix.

### Instructions
1. Run `Get Brain Data.ipynb` first to generate the necessary CSV file.
2. Open and run `ML Classification.ipynb`.

---

**Notes:** 
- Ensure that you have unzipped the `raw_data.zip` to a folder called 'data' before running the notebooks.
- The generated CSV file (`brain_data.csv`) contains information about the number of CSF, GM, and WM pixels for each participant, along with their age and gender.


## Data Information:
[Link to Data on OneDrive](https://dalu-my.sharepoint.com/personal/fr591304_dal_ca/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Ffr591304%5Fdal%5Fca%2FDocuments%2FData%2FBrain%20Age%20Data&ga=1)

There are 4 folders: 652 Healthy Inividuals (330F, 322M)
- 98 x 116 x 94 voxels (2mm x 2mm x 2mm spatially)
- `meta` contains subject_id, **age**, and sex for all 652 subjects.
- `images` contains brain MRI scans for these 652 subjects
- `masks` contains brain masks for these 652 subjects
- `segs_ref` contains segmented brain scans (GM,WM,CSF) for these 652
    - Ground Truth Data


## Resources: (More in PowerPoint Presentation)
- Presentation video: https://dalu-my.sharepoint.com/personal/fr591304_dal_ca/_layouts/15/stream.aspx?id=%2Fpersonal%2Ffr591304%5Fdal%5Fca%2FDocuments%2FDal%2FPresentations%2F2024%2FNeuralHackathon%2Fvideo2057952459%2Emp4&ga=1&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview
- Neural Data Science Textbook: https://neuraldatascience.io/intro.html
- CNN's with Keras: https://www.kaggle.com/code/kanncaa1/convolutional-neural-network-cnn-tutorial
- Data Visualization: https://simpleitk.org
- ResNet: https://blog.paperspace.com/writing-resnet-from-scratch-in-pytorch/
- Clustered-FL-BrainAGE: https://github.com/Abtinmy/Clustered-FL-BrainAGE
- Medical Imaging Analysis w/ PyTorch: https://medium.com/dair-ai/medical-imaging-analysis-mri-cnn-pytorch-4877e64e7303