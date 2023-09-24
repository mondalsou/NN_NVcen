# NN_NVcen
Machine Learning Model for Material's Property Prediction


Goal: Magnetic property of a material depends on the Temperature they are measured. On the other side, Temperature directly affects the material structure. The last sentence suggests that atomic displacement (the position of the atoms in materials) is a function of Temperature. Once you displace the atoms, the magnetic property also changes. Quantum Mechanical Calculations can predict magnetic properties (such as D tensor ) as a function of atomic displacement. However, this process can take years. For example, we required 600K heavy Quantum Mechanical Calculations. Hence, we want to propose a machine-learning model which can predict magnetic properties (D tensor) as a function of atomic displacement.


Details of the Work:

* The training set has been constructed by calculating D tensor over 2000 atomic displacements.
* 2000 Quantum Mechanical Calculations have been performed using automated Shell Scripts and Python programs.
* Python has been used for Data cleaning and wrangling in the course of training set preparation.
* Built efficient Neural Network Model using Keras
* The neural network we used has 3 hidden layers consisting of 128, 64, and 16 nodes.
* The input layer has N nodes, where N is the number of atoms present in the material.
* The output layer has 9 nodes which represent the 3x3 D tensor (representing magnetic property)
* Each hidden layer has a sigmoid as an activation function and L2-regularization.
* Among 2000 data points, 1800 were used for training and while 200 for validation.

Peroformance:
* The measured RMSE value for the validation set is in the order of 1.8E-04, which shows the very high accuracy of the predicted Model.


Comparison of *Machine Learning Prediction* and *Qunatum Mechanical Simulation* results of D tensor for different atomic displacement.
Both i and j of the *Dij* runs from 1 to 3. Nine columns of the figure represent all the 9 elements of D tensor. Each row represents *D* tensor as a function of the atomic displacements for different atoms.

* RED point = Quantum Mechanical Simulation Result
* BLUE point = Machine Learning Prediction

![alt text](https://github.com/mondalsou/NN_NVcen/blob/main/SI-10.png)
