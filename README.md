### Predicting a Subject’s Card with the Muse-S Headband ###

### Description

In this project, we have developed a Brain-Computer Interface system to predict the card a subject is focusing on in real-time with P300 evoked potentials (P300 EPs) recorded with a Muse-S headband. Firstly, we built our dataset, named 4-card dataset: we told subjects to focus on one out of four cards, then showed the cards in intervals of 200 ms, labelling differently the P300 EPs whether the subject was focusing on the current displayed card or not. Secondly, we tested different models to filter and classify the P300 EPs by telling subjects to focus on a card of their choice, then showed cards in intervals of 200 ms to see which one evoked the P300 EPs that correspond to focusing. We conducted offline classification using an existing dataset in order to analyze the performance of several models. Afterwards, we conducted offline classification on
the 4-card dataset using the models that performed satisfactory on the existing dataset and some new models. The best model for the existing dataset (obtaining a precision of 0.32 and a recall of 0.69) and for the 4-card dataset (with an average precision of 0.65 and an average recall of 1) used ERP covariances and Xdawn for spatial filtering and Logistic Regression for classification. Lastly, we tested this model for the real-time experiment, obtaining an average precision of 0.07 and an average recall of 0.71.


### Flowchart of the project

![image](/uploads/2c3210f3cceb2f71ebbcf17671e3644f/image.png)


### Dependencies & steps to run the code

We used Python programming language, version 3.7.

The following libraries are necessary:
- Muse LSL - a Python library for communicating with the Muse-S
- Pyriemann - Python library for Riemannian Geometry 
- MNE-Python - Python library for processing EEG data
- Timeflux - Python library for real-time processing
- PsychoPy - Python library used to develop the GUI for our experiment
- Scikit Learn - Python library for machine learning
- Numpy - Python library for managing mathematical operations
- Pandas, Matplotlib, Seaborn - Python libraries for visualizing and analyzing the data
- MOABB - an open-source framework with multiple EEG datasets - used for offline classification 

We recommend to install the library EEG notebooks, as it contains all the necessary packages. 

Installation instructions: https://neurotechx.github.io/eeg-notebooks/getting_started/installation.html

Before running our code, turn on the Muse-S device and connect it to the computer by typing "muse lsl stream" in a command prompt terminal.

After installing EEG notebooks, you will have a new Pyhton environment. Run the code in this environment by opening a command prompt terminal and typing the following:

timeflux app_name.yaml -d -e SESSION="session_name" -e SUBJECT="subject_name"

Press A to start saving data. When you think you have enough data, press S. 



