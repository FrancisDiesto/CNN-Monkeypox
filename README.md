PROPONENTS

DIESTO, Francis Ryan
MACAN, Kiana
TALE, Blessy

========================================================================

This project is a learning evidence output for the course subject
specified above. This project was submitted A.Y. 2022-2023.

========================================================================

CNN-MONKEPOX-CLASSIFIER

- To start of I changed the tensorflow settings to change memory consumption from CPU to GPU
- we then mounted the google drive account that serves as my directory, it contains the dataset of 'Monkeypox Skin Lesion Detection using Deep learning'
- we then loaded that data and used a numpy iterator to change change batch sizes an image 
classified as 1 is others while 0 signifies monkeypox
- We then build the model we have our input sizes shaped depending on the image height and width
 and by using keras sequential we make convolutional layers with 16 filters 
sized 3x3 each with a stride of 1, they also have a 'relu' activation function which turns 
negative numbers from the feature map to zero. 
- After each convolutional layer is a max pooling layer in its default size this helps for 
dimensionality reduction which takes the most significant features from each feature map.
- dropout layers were also added which randomly takes 3 out of 10 values and drops them. this 
helps in dealing with overfitting. 
- After the convolution hidden layers we have our flattening layer which turns the matrices into
1d array making it ready for our dense layers. 
- we have 2 dense layers the last layer is sigmoid as it will only give one output: "monkepox" or "others"
- we used 'adam' as our optimizer and tracked the accuracy metric
- we then trained the model by fitting it with our data. 
- we had it run for 50 epochs 
- then plotted our training and validation loss to see if there is a significant gap between them
- accuracy was also plotted. 
- we now tested it using the testing batches
- then checked its confusion matrix
- and additionally outputted its metrics (precision, recall, accuracy)
- Just for a test we tested it with images outside of the dataset and it returned with a satisfactory
result.
