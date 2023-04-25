# CNN-Brain-Tumor
Using CNN architecture to detect and classify brain tumor:

• Motivation:

Brain Tumor is prevalent among both children and adult. Early 
diagnosis and treatment has proved to improve the life expectancy of patients. 
The detection of brain tumor is a very critical task. The best technique to detect 
brain tumors is Magnetic Resonance Imaging (MRI). These are examined by 
radiologists. These manual examinations are error prone due to the abnormalities 
in the sizes and location of the brain tumors. We can improve the accuracy of 
tumor detection by developing a CNN model. 
• The dataset we are using has images related to three different brain 
tumors(glioma tumor, meningioma, pituitary tumor). Therefore, this model can 
help detect the presence of these three tumors.

Plan about how to implement your project:

The CNN model designed for brain tumor classification using MRI images consists 
of several major components. The input layer takes a 2D image of size 224 x 224 
pixels. there are three convolutional layers applied that use 32 filters of size 3 x 3, 
with a stride of 1, with no padding and 'ReLU' activation function. A max-pooling 
layer is used to reduce the spatial dimensions of the output after each convolution 
layer.A dropout layer is added after the convolution layers followed by flattening 
the images. Two fully connected layers are implemented with a softmax output 
activation function. To prevent overfitting, a dropout layer is added gain to the 
output of the first fully connected layer. The hyper parameters of the model include 
the learning rate, number of epochs, batch size, dropout rate, and activation 
function. The default values of these hyper parameters are Learning rate: 0.001, 
Number of epochs: 10, Batch size: 32, Dropout rate: 0.5, Activation function: 
ReLU. In this model we will be using Gridsearch to tune these hyper parameters.

The dataset we used: https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumorclassification-mri

Data splitting and performance evaluation for your CNN model: 

The data is available as train and test data in two different folders respectively. We 
will be transforming the data and loading them in batches using data loader. The 
model is trained using the train data.
We will be using the test data to evaluate the performance of the model i.e, the 
accuracy of the trained model on test dataset.

Data augmentation for increasing your sample size in the training set:

For data augmentation we will rotate the image by a random angle, which creates 
new samples with different angles and it increases the diversity of the dataset and 
it will help the model to recognize the same object at different angles
