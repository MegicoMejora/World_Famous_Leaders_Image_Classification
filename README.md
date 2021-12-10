# World_Famous_Leaders_Image_Classification
### Deep Learning project using OpenCV library.

The steps involved in creating this project,
1. Dataset Creation
2. Image Preprocessing 
3. Feature Extraction
4. Model Building

## Dataset Creation

The dataset was created by downloading the World famous leaders images using the **Fatkun chrome extension**. 
The dataset consists of images of 10 famous leaders. Images were downloaded for each of the leaders and each image is in 'jpg' format.

## Image Preprocessing

During image preprocessing, the images were converted into gray images. Next step is to detect the face and eyes in the image. Face detection is done by using the Haar Cascades features.
Once the face is detected,it will detect eyes, if two eyes are detected then that image will be cropped and saved and the other images will be discarded.
Also, the images which had multiple faces or not clear or obstructed images were cleaned. 
The cropped images were stored in the folder 'cropped_images datasets'. 

## Feature Extraction

Wavelet transform function is used to extract the facial features from the images.

Using the Wavelet transform function extracted the features for all the cropped images and created X and y.
Where X will have all the raw images and the transformed wavelet images stacked vertically. 
Created a class dictionary and assigned numbers to each leaders names. And, y will have the numbers that are assigned to the Leaders names.

## Model Building

The model was trained using different candidate models with different parameters. Using GridSearch the best model with best parameters were obtained.

The candidate models are,
1. SVM
2. Random forest
3. Logistic regression

