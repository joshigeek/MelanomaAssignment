# Melanoma Detection
Melanoma is a type of cancer that can be deadly if not detected early.

The data set used in this contains the following diseases:

* Actinic keratosis
* Basal cell carcinoma
* Dermatofibroma
* Melanoma
* Nevus
* Pigmented benign keratosis
* Seborrheic keratosis
* Squamous cell carcinoma
* Vascular lesion

## Problem Statement
To build a CNN based model which can accurately detect melanoma. 

Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.


## Project Pipeline
* Data Reading/Data Understanding: Defining the path for train and test images 
* Dataset Creation: Create train & validation dataset from the train directory with a batch size of 32. Also, make sure you resize your images to 180*180.
* Dataset visualisation: Create a code to visualize one instance of all the nine classes present in the dataset 

* Model Building & training: 
  - Create base CNN model:
    - No dropouts used
    - Over-fitting was observed
  - Model 2: With dropouts
    - Adding dropout layer helped to control over-fitting
    - Accuracy wa low now, arond ~65%
    - Class imbalance was observed
  - Model 3: using Data Augmentation
    - Augmentor library was used, to reduce class imbalance
    - Added one more layer of 128 to increase accuracy further

## Results
### Model 1
* loss: 0.2452
* accuracy: 0.9018
* val_loss: 2.2153
* val_accuracy: 0.5459
### Model 2
* loss: 1.0756
* accuracy: 0.6088
* val_loss: 1.3164
* val_accuracy: 0.5347
### Model 3
* loss: 0.1513
* accuracy: 0.9379
* val_loss: 0.5078
* val_accuracy: 0.8656

## Final analysis:
Overall model is improved and accurary and validation accuracy of model has improved, following are the factors which has helped to imporve model:

Dropout layer: Helped to get rid of over-fitting
class Rebalance: This helped to increase the model accuracy
Adding extra layer of 128: That has helped to increase the accuracy beyond 85%

### Contributed by:
* Himanshu Joshi