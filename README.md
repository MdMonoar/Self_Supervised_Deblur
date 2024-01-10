<h1 align='center'>Self Supervised Deblurring</h1>
In this project a self supervised deblurring model was built for deblurring blurred images. Then a previously made semantic segmentation model was applied to segment different objects.

## Data Source
The data which is used for this project is a popular dataset named CamVid(Cambridge-Driving Labeled Video Database). It was taken from popular data repository Kaggle. It consists of over 700 images and masks for semantic segmentation. 
The images and masks were seperated in training, validation and testing sets. The ground truth label associate each pixel with one of 32 semantic classes.

## Procedure
- A blur function was built which applies random level of gaussian blurring to each image 
- All images were blurred using the blur function
- Then the training and validation images were blurred again.This batch was used for training the self-supervised model and the previous batch was as ground truth 
- A self supervied deblurring model was built and trained
- Test images were deblurred using the trained model
- The performance of the segmentation model(previously made) was comapred with original test images and newly deblurred images.
