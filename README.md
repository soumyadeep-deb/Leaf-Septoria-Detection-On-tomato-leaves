# Leaf-Septoria-Detection-On-tomato-leaves
Leaf Septoria is a disease that effects tomato plants quite often. 

We used CNN here to detect that disease.

# More on the project
### Augmentation methods used:
1. Rotation by 30 degrees
2. Shifting along the width
3. Shifting along the height
4. Shearing the image
5. Horizontal & Vertical flip
6. Introducing different lighting conditions

Fill method used: 'nearest'

### Model Description:
We have used a Convolutional Neural Network with 3 Convolution and 3 MaxPool layers.

Dropout was introduced in the Dense layers as follows:
1. 40% Dropout before Flattening
2. 15% Droput before the first hidden layer
3. 25% Dropout before the Output layer

### Information on the dataset:
Actual Dataset: https://www.kaggle.com/emmarex/plantdisease

Download the dataset, from there extract these two files: Tomato_Septoria_leaf_spot, Tomato_healthy

**Now, we create train & validation sets manually.**

There are 3362 images in total.

So, if you want valid_set size = 0.2 i.e. 20% of the data, then you'll have to select a total of 672 images for the validation set.

Steps:
1. Make a folder ***valid*** and 2 other folders ***Healthy leaf*** and ***Septoria Leaf***.
2. Then we randomly select 312 images from ***Tomato_healthy*** folder and move them into ***Healthy leaf*** folder.
2. We randomly select 360 images from ***Tomato_Septoria_leaf_spot*** folder and move them into ***Septoria Leaf*** folder.
3. Then move the ***Septoria Leaf*** & ***Healthy leaf*** into the **valid** folder.

Your validation dataset is complete!

Now, make 2 more folders of the same name: **Septoria Leaf** & **Healthy Leaf**

Move the remaining images into the respective folders and place these two folders in a new folder **train**

**Your dataset is complete!**

Upload the train and valid data into your Google Drive and mention the paths after the drive is mounted on Google Colab.
