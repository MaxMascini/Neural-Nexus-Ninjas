# Neural-Nexus-Ninjas
Neural Nexus Ninjas Neural Data MRI Hackathon Repository

# Tasks:
1. [Easier] Use CNN (Kerras(?)) to find relationship between gray matter, white matter, and cerebrospinal fluid with age
    - Could calculate this information and then use it as a feature with a classifier to predict age directly
2. [Harder] Use ResNet to predict age directly from MRI data


## Data Information:
[Link to Data on OneDrive](https://dalu-my.sharepoint.com/personal/fr591304_dal_ca/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Ffr591304%5Fdal%5Fca%2FDocuments%2FData%2FBrain%20Age%20Data&ga=1)

There are 4 folders: 652 Healthy Inividuals (330F, 322M)
- 98 x 116 x 94 voxels (2mm x 2mm x 2mm spatially)
- `meta` contains subject_id, **age**, and sex for all 652 subjects.
- `images` contains brain MRI scans for these 652 subjects
- `masks` contains brain masks for these 652 subjects
- `segs_ref` contains segmented brain scans (GM,WM,CSF) for these 652
    - Ground Truth Data

## ACEnet Login Info:
https://jupyter.neuraldh.ace-net.training

pw: actually.grossly.patient.iguana

ssh: userXXX@login1.neuraldh.ace-net.training

## Resources: (More in PowerPoint Presentation)
- Presentation video: https://dalu-my.sharepoint.com/personal/fr591304_dal_ca/_layouts/15/stream.aspx?id=%2Fpersonal%2Ffr591304%5Fdal%5Fca%2FDocuments%2FDal%2FPresentations%2F2024%2FNeuralHackathon%2Fvideo2057952459%2Emp4&ga=1&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview
- Data Visualization: https://simpleitk.org
- ResNet: https://blog.paperspace.com/writing-resnet-from-scratch-in-pytorch/
- Clustered-FL-BrainAGE: https://github.com/Abtinmy/Clustered-FL-BrainAGE
- Medical Imaging Analysis w/ PyTorch: https://medium.com/dair-ai/medical-imaging-analysis-mri-cnn-pytorch-4877e64e7303
