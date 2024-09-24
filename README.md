# ChestXRayCNN

BUSINESS GOAL

This machine learning project demonstrates how neural networks can be used to detect COVID-19 in patient X-rays. The model can then be built upon in order for practical use or further
research. 

COVID-19 tests are often carried out using test kits and swabs. Within clinics, X-rays can be used for patients who are at higher risk of developing complications from COVID, or are 
more likely to develop long COVID. The use of a machine learning model can help doctors to speed up and validate their diagnoses, giving them more time to treat their patients. 

DATASET

The model uses the dataset 'Chest X-ray (Covid-19 & Pneumonia)' from the data science platform Kaggle (https://www.kaggle.com/datasets/prashant268/chest-xray-covid19-pneumonia).

MACHINE LEARNING MODEL 

Two neural network models were used to train the medical X-ray images (ResNet and VGG). These two networks were chosen due to their usage in the following paper: 
COVID‑19 detection from chest X-ray images using transfer learning (https://www.nature.com/articles/s41598-024-61693-0). As a result, the model choices reflect those being currently
used within medical and machine learning research. 

For time and space efficiency, ResNet-18 was chosen over VGG. Even with GPU usage, VGG took several hours longer than ResNet. In the case of medical diagnoses, fast runtimes are 
important as there may be several patients and the diagnoses should be made as early as possible so treatment plans can be decided and discussed. 

The X-ray images are resized before being passed into the neural network. Transformations are applied to diversify the images that the network is being trained on.

The dataset is imbalanced, with a smaller number of COVID-19 X-rays, therefore class weighting is used within the model (to still include that class when training). 

HYPERPARAMETER TUNING 

Optuna, a hyperparameter optimisation framework, is used to carry out Bayesian Optimisation on the ResNet model and in turn improve model performance. 

The learning rate, l1 lambda and l2 lambda values of the neural network are optimised. The learning rate and weight decay (l2 lambda) values are then updated in the 
model optimiser in the main notebook.

The model was set to use 4 epochs and a batch size of 64 due to memory requirements, however, in a business context the clinic should have computers with more GPU resources available. 
In turn, an epoch setting of 50 to 100 would be more effective. 

MODEL RESULTS

The ResNet model achieved a recall of 80.35%, suggesting that the model performs moderately well and has a low number of classified false negatives. This is important in medical models: missing 
the diagnosis of disease in a patient is more significant than diagnosing a patient when they do not have the disease. 

The model gives an overall accuracy of 83.62%. 

There is however, room for improvement, which could be further achieved by more hyperparameter tuning (the final accuracy should be in the high 90s).

CONCLUSIONS

This model showcases a straightforward example of how a neural network model can be used to diagnose COVID-19 in patient X-rays. Approaches such as these can be applicable in clinics 
which provide treatment for patients with COVID-19, however the model would have to be built upon before being deployable.


FURTHER ACTIONS 

- Referencing the current medical research, including the network architectures used, and design neural network architectures from scratch for the particular clinic
- Gathering X-ray data at the particular clinic, instead of using publicly available datasets. The dataset should be ensured to be as balanced as possible 
- Improving upon hyperparameter tuning methods to use more complex approaches 

RUNNING THE CODE 

The main code can be found in the ResNet folder. 

The code for the VGG model can be viewed in the VGG folder. 

The label txt files are loaded within the ResNet and VGG model notebooks respectively.

The code for the Optuna hypeparameter tuning (Bayesian optimisation) can be viewed in the Hyperparameter Tuning folder.

The datasheet and model card files are also provided in the folder. 
