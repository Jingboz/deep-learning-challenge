# Module 12 Report Template

## Overview of the Analysis

The analysis is mainly for establishing a machine learning model to help Alphabet Soup select the applicants for funding with the best chance of success in their ventures. The model produced gathers the dataset in different categories to create a binary classifier that can predict whether applicants will be successful.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Data Preprocessing
  * The target of the model is "IS_SUCCESSFUL" which indicates whether the applicants were successful in their ventures.
  * The features for the model are "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS" and "ASK_AMT".
  * Whereas "EIN" and "NAME" are not relevant to the results of the applicants. They are independent from the success of applicants.

* Compiling, Training, and Evaluating the Model
  * The model consisted of two hidden layers and one out put layer. The first hidden layer has 60 neurons and a activation function of "relu", and the second one has 100 neurons as well as "relu" activation function. Output layer has one neuron and "sigmoid" activation function since the result we expect is a boolean or binary classification, which is suitable for "sigmoid" function to deal with. 
  * Unfortunately, the requirement of 75% accuracy did not meet from this model. The maximum accuracy it could get is 73.15%.
  * In order to increase the performance of this model, I tried to adjust the number of epochs to avoid any over-training or under-training. Finally, 15 epochs is the optimal number for this model and dataset. I have also tried to modify the neuron numbers for each hidden layers. If more nodes are added, the model will be trained very slow and will rely on the training dataset in a small number of epochs. On the other hand, if there are few nodes in each layer, the model will be still under-trained after a large number of iterations. The activation function is the last variable I touched on, but the results are not improved much as expected.

## Summary

Overall, this model is still a prototype for solving the problem of selecting potential successful applicants. It has a accuracy of 73.15% which is not very good as we are expecting 75%. The loss value of this model is not good either, which means the discrepancy between the predicted output and the expected output has about 55% loss. To further improve this model, adding more hidden layers can be considered. However, more layers will make the model more complicated, which will easily lead to over or under training.