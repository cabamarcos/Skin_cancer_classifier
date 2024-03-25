# Skin Lesion Diagnosis System
## Introduction
In this practice, we will implement a system for diagnosing skin lesions based on dermatoscopic images.

Before delving into the practice, we will briefly describe the database we will use and the problem we aim to address.

Our objective is to implement a Convolutional Neural Network (CNN) that provides an automatic diagnosis of skin lesions from dermatoscopic images. Dermoscopy is a non-invasive technique that allows the evaluation of structures not visible to the naked eye, which specifically correlate with the histological properties of lesions. Identifying specific visual patterns related to color distribution or dermatoscopic structures can aid dermatologists in deciding on the malignancy of a pigmented lesion. The use of this technique greatly assists experts in supporting their diagnosis. However, the complexity of its analysis limits its application to experienced clinicians or dermatologists.

In our scenario, we will consider three classes of lesions:

- Malignant Melanoma: Melanoma, also known as malignant melanoma, is the most common type of skin cancer and arises from pigment-producing cells known as melanocytes. Melanomas typically appear on the skin and rarely in other locations such as the mouth, intestines, or eye.

- Seborrheic Keratosis: Seborrheic keratosis is a non-cancerous (benign) skin tumor that originates in the cells of the outer layer of the skin (keratinocytes), making it a non-melanocytic lesion.

- Benign Nevus (Mole): A benign skin tumor originating from melanocytes (melanocytic).

## Dataset Description
The dataset has been obtained from the 'International Skin Imaging Collaboration' (ISIC) archive. It contains 2750 images divided into 3 sets:

- Training Set: 2000 images

- Validation Set: 150 images

- Test Set: 600 images

For each clinical case, we have two images available:

- Dermoscopic image of the lesion (in the 'images' folder).

- Binary mask with segmentation between lesion (mole) and skin (in the 'masks' folder).

Additionally, there is a CSV file for each dataset (training, validation, and test), where each row corresponds to a clinical case, defined with two fields separated by commas:

- The numeric id of the lesion: which allows defining the paths to the files containing the image and the mask.

- The label of the lesion: available only for training and validation, being an integer between 0 and 2: 0: benign nevus, 1: malignant melanoma, 2: seborrheic keratosis. In the case of the test set, labels are not available (their value is -1).

To get the dataset you can download it from here: https://drive.google.com/drive/folders/165KaDSlh51DFtulsZVFhFWYFFbCc1yov?usp=sharing

