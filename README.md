# Video-Object-Detection

#### Data preperation
* Raw Image and Annotation files used to create train and test csv and tfrecord files are uploaded in pistol_data folder.
* The xml annotation files are parsed on the features and a corresponding csv files are created.
* The csv and tfrecord files generated can be viewed in [gdrive](https://drive.google.com/drive/u/0/folders/17dJMRMj5-QBFoHV9mfgi8Xw8QqyCzPyR)
* This data contains black and white images and rotated images for a better accuracy.
* Object_detection.pynb has the code used for this conversions.

#### Efficientnet model training
* Using a pretrained checkpoint , efficientdet_d0_coco17_tpu-32.tar.gz, we are training the model with pistol and knifes datasets created.
* Number of steps are taken as 40,000 and num_eval_steps is taken as 500. The more steps, the longer the training. Increase if your loss function is still decreasing and validation metrics are increasing.
* Update the configuration file to take number of classes which should be identified i.e, knife and pistol in this case and update hyperparameters like fine tuned checkpoint path, train tfrecords path, test tfrecords path and labelMaps paths.
* Train the model with new configuration and data. This takes approximatly 5 hours.
* Save the trained model.


