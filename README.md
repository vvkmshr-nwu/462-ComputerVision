# 462-ComputerVision
Final Project for MSDSP 462-ComputerVision.
To understand how code files are organized please read below:

The project has been completed in Multiple parts.

1. The EDA folder contains notebook for EDA performed and Results.
2. Code_CNN contains notebooks for CNN Model trained from Scratch
3. Code_Pretrained_Models has codes for Restnet, EfficientNet and Mobilenet Models. For each of these models there are three cases tested, and each case is stored in a subfolder as described below
   
   3.a. Pretrained_custom_classfier:The include_top=False argument used in the code removes the fully connected (dense) layers that are normally present at the top of the ResNet50 model, which are responsible for classification on the original ImageNet dataset (1000 classes). By removing the top layer, only the convolutional base of ResNet50 is retained, which acts as a feature extractor. The new dense layers was added is being trained for a custom task (e.g., binary classification), while the ResNet50 base extracts powerful features from the input images.
   
   3.b. Pretrained_RandomForest_Classifier: Over here for each of the model, the classifier in the base model is changed to Random forest and then trained and tested.
   
   3.c. Last20LayersTrainedModels: In this case last 20 inner layers of pretrained model are set to 'Trainable' and then exposed to the training dataset, and then the new trained models are run for test cases. 
