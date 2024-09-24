Model Card

MODEL DESCRIPTION
MODEL INPUTS: Images (JPG file type) of dimension 224 x 224. 

MODEL OUTPUTS: Three classifications (one neuron for COVID-19, one for PNEUMONIA, one for NORMAL).

MODEL ARCHITECTURE: ResNet-18 neural network architecture. The layers other than the classification layer are frozen, so that there are less parameters to update. 
		    The architecture is pre-trained for ease of use. The last layer is a linear layer with 512 neurons and an output of 3 neurons. 

PERFORMANCE

The model gives a recall of 80.35% on the test set. This is calculated using scikit-learn's recall_score library. This is to determine how many incidents of false negatives
the model calculates. The model should have a low number of false negatives (of not diagnosing a patient with COVID-19 when the X-ray does contain COVID-19). Otherwise, many
patients with COVID-19 would not get the treatment needed from their doctors, if the model was to be improved and used in a clinic. 

The model gives an overall accuracy of 83.62% on the test set. Therefore, the model is generally effective at diagnosing COVID-19 within patient X-rays. 

The model would need to be improved by around 10-15% before being able to be clinically confident in using the model results (in the real world).

LIMITATIONS

A model is often only as good as its data, and the dataset is imbalanced - class weighting had to be used on the model because there are a smaller number of COVID-19 X-ray
instances. This did however improve the model accuracy and scores.

The model is also limited in that it can only classify COVID-19 (and pneumonia) - it cannot diagnose specific strains of COVID or make any other observations about the
COVID-19 in the patient X-ray.

TRADE-OFFS

There was a trade-off between runtime and GPU memory usage, with model performance. The batch size and epoch number for the model had to be decreased, and a lower number of 
trials had to be run during the Optuna hyperparameter optimisation. As a result, the model did not get to improve as much as it could have. 

POTENTIAL IMPROVEMENTS
- Balance the dataset by adding more examples for COVID and NORMAL
- Do some post-evaluation on the images, to understand how the neural network is analysing the images (for example, GradCam)
- Run more hyperparameter tuning (more configurations and more complex optimisation)