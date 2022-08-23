# Microorganism-images-classifiers
This repository contains the work developed by Gorka Buenvarón, under the supervision and guidance of Idan Tuval and Mary Kane (IMEDEA) and Francesc Bonin (UIB). FOUNDED BY CSIC, JAE PROGRAM. FINANCIADO POR CSIC, PROGRAMA JAE.

In this repository, you will find two different image classifiers, the image datasetsts used to train them, a brief report of their performance, and useful script used to prepare your images. 

The first classifier, is a keras trained model that uses image classification to classify input images as Phytoplankton, Consumming Zooplankton, and Non-Consuming Zooplankton. This produces a csv file with the labels. It is known as "phase 1" classifier, as it allows to discriminate phytoplnakton to be classified in the next classifier.

The second clasifier is a more complex model, based on bounding boxes, that finds, for the imput images, all the individual phyto organisms, and the group they belong to, namely, Dinoflagelates, Diatoms or Chlamy.

Other scripts included are the colab notebooks used to train the models, that can be used with other training dataframes to improve results or develop differnt classifiers. Scripts used to change image formats are also included, if the user needs it.

