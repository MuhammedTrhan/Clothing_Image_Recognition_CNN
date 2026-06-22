### **Phase 0: Environment Setup & Weights & Biases**

Since using wandb is mandatory and you need to upload your runs, let's get that out of the way first.

* **Terminal Login:** Open your VSCode terminal and type `wandb login`. Press Enter. It will prompt you to paste your API key (which you can find in your wandb account settings online).
* 
**Project Variables:** Since you are already in the EiDL wandb team, you will need to set up your project strings in your Python script like this:


* 
`PROJECT = Übungsgruppe_Vorname1_Name1_Vorname2_Name2` 


* 
`run_name = f"run_id_changed_parameters_timestamp"` 





### **Phase 1: Dataset Analysis**

Before feeding data to a model, you need to understand it.

* Load and explore your crowdsourced dataset containing images of T-Shirts, Pants, Socks, Shorts, and Long-sleeved items.


* Count and report the number of images per class.


* Visualize sample images from every single class.


* Analyze the distribution of image sizes, aspect ratios, and color channels.


* Identify any potential dataset challenges, such as class imbalance or poor image quality.


* Split the dataset: 80% for training, 10% for validation, and 10% for testing.



### **Phase 2: Data Preprocessing**

Here, you will get the data ready for the neural network.

* Implement data augmentation techniques on the training set, including random cropping, flipping, rotation, and color jittering.


* Normalize the images using the specific mean and standard deviation of your dataset.


* Create PyTorch DataLoader objects for your train, validation, and test sets.


* Visualize some of the augmented images to double-check that your preprocessing steps are working correctly.



### **Phase 3: CNN Implementation**

Time to build the brain of the operation.

* Implement a CNN architecture entirely from scratch using PyTorch.


* Include multiple convolutional layers (with activation functions and pooling), fully connected layers for the output, and Dropout layers to prevent overfitting.


* Ensure that your total parameter count strictly does not exceed 800,000 parameters.


* Document the justifications for your architectural choices, such as filter sizes and the number of layers.



### **Phase 4: Model Training**

This is where the learning happens.

* Define a suitable loss function and an optimizer.


* Train the CNN on your training set while using the validation set to monitor performance and prevent overfitting.


* Implement early stopping based on the validation loss metric.


* Plot the loss and accuracy curves for both training and validation over the epochs.



### **Phase 5: Model Evaluation**

Let's see how well your model actually performs.

* Evaluate your fully trained model against the test set.


* Calculate and report the overall accuracy.


* Calculate and report class-wise metrics: precision, recall, and F1-score.


* Generate a confusion matrix.


* Analyze the images your model misclassified and discuss the potential reasons why it made those mistakes.



### **Phase 6: Submission**

Put it all together before the deadline. Late submissions will not be accepted.

* Write a one-pager (PDF, 12 pt font) summarizing your approach, CNN architecture, hyperparameters, preprocessing steps, training curves, metrics, misclassification analysis, and any challenges you faced.


* Package everything into a ZIP file containing your Python code, trained model weights, and the one-pager PDF.


* Be prepared to present these results in the exercise session.



---

Shall we kick things off with Phase 1 and look at the code required to load and split your crowdsourced dataset?