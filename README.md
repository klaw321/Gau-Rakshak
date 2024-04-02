# Gau-Rakshak
This is a Python script that implements a Convolutional Neural Network (CNN) model for detecting wheat diseases. It begins by importing necessary libraries and setting the paths for the dataset and images to be classified, which belong to 6 categories; healthy, leaf rust, crown and root rot,fusarium headblight ,yellow rust and loose smut. The dataset is loaded and preprocessed, converting the images into numpy arrays and normalizing their values. The data is then split into training and testing sets.

The CNN model is created using the Sequential model from Keras. It consists of multiple convolutional and max-pooling layers to extract features from the input images, followed by dense layers for classification. The model is compiled with appropriate settings such as optimizer, loss function, and accuracy metric. Data augmentation is applied to the training images using the ImageDataGenerator class from Keras, which introduces random transformations to increase the diversity of the data. The model is trained using the augmented data and the fit() function. After training, the model's performance is evaluated using the testing set. The accuracy and loss values are displayed.

The model is then used to classify new images by preprocessing them and predicting their labels. The predicted labels, along with the corresponding image names, are printed.
Similiary we have created Resnet50,VGG16,Mobilenet transfer learning model inorder to compare the accuracy with our cnn model.

Finally, the trained model is saved in the H5 format  as well as into tflite model for future uses .
About
This model in Trained on over 5K images of wheat plant.
The dataset is trained in 158 Batch Set, each containing 32 Images
For resizing, images are converted into 256x256 dimension with 3 channel colors
For max pooling 2D dimension kernel are used
For convoultion layer 3D dimension layer is used
For intergration in Mobile Devices
To integrate the model in Mobile device TFLite is used
TFLite model can be found in this repo : Flutter Application [https://github.com/Netesh5/gahu_rakshak]
We can implement the model using offical Tensor flow package
For preprocessing the image to upload in flutter application
Before fitting the image directly into the model, it need to preproccessed
We need to convert the image into 256x256 with 3 channel
Then we need to convert the 3D images data to Tensor Array of Float32 or Unit8 type
After the above step we can run data into binary form and fit in model
