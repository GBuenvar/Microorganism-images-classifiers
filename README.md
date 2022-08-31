# Microorganism-images-classifiers
This repository contains the work developed by Gorka Buenvarón, under the supervision and guidance of Idan Tuval and Mary Kane (IMEDEA) and Francesc Bonin (UIB). FOUNDED BY CSIC, JAE PROGRAM. FINANCIADO POR CSIC, PROGRAMA JAE.

In this repository, you will find two different image classifiers, the image datasetsts used to train them, and useful script used to prepare your images. 

## image classification

The first two folders, Phyto-Zoo class and Phyto-Zoo-Spo class, contains the notebooks needed to classificate any input image folder into tree or four groups. The first one just separates all type of phytoplankyton from Consuming (Zoo that ate Phyto) and Non consuming (empty) Zooplankton. The second also classifies infected phytoplankton and sporangias (full and empty) into a SPO group. The "prediction" notebook is the one to be used for clasification. Save the notebook and the trained model (keras_model_efficientnetv2-b3-21k_epoch_10) to your drive. In the notebook, you have to indicate the path to the model and the folder in which you want to save your outputs. The notebook itself contains the instructions to follow.

If you want to go further and train your own model, there is also included a training notebook, that easily can be follow to train a similar model and evaluate its performance. The idea with this notebook is to provide the original work followed to obtain my results and also a friendly enviroment to develop new models.

## Microorganism detection and clasification


The second clasifier is a more complex model, based on bounding boxes, that finds, for the imput images, all the individual phyto organisms, and the group they belong to, namely, Dinoflagelates, Diatoms or Chlamy. The idea is to use the images clasified as "phyto" in the previous clasifier to one step deeper into the specific phyto species in your sample. The inference notebook provides a easy way to process your sample. It just needs the trained weights that can be found in this folder, the drive folder where images to be procesed are stored, and and output directory to save your results. The results can be obtained in three different formats: The processed images indicating the found organisms and the species they belong to, and/or txt and/or json files, indicating the name image, the object found (in x,y image relative coordinates from 0 to 1), the class they belong to and the % of confidence with that class.
Training and evaluation notebooks are also provided on this folder in case you want to extend the dataset or try your own.

## Other scripts

In order to make your life easier, I have also include a simple python code that transform tif images to png and jpg format.

## useful sites and tools

For image clasification, i found very usefull The TensorFLow hub site https://tfhub.dev/. My own clasificator is based on one of the models that can be found there. 

For object detection, I have used YOLOv4 in the Darknet framework. The reason is that YOLOv4 provides a sufficient perfomance for our porpose, and darknet framework is easily understood and is provided by the YOLOv4 author. It is posible to export the model to other frameworks if you prefer that. Ohter site that was very usefull to data preprocessing was Roboflow. They provide simple tools to work with datasets. Also, for image annotation, labelImg was the tool I used for this dataset, it is easier and more intuitive than The Roboflow image annotation tool.



