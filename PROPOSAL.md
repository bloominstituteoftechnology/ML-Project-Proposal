# ML Project Proposal
- Alex Strebeck
- Object Detection and Orientation (ODO)

## What track are you choosing (analysis or engineering)?
Engineering

## What is your data source?
Created data sorce, gernerated pictures.

## Summarize the status of your data and what cleaning is needed.
Data will be clean, but labeling will be needed. Want to find a way to label the images fast.

## Summarize the structure of your data and what models/techniques work with it.
Data would be a bunch of images. I would be retraining a yolo V3 model in order to detect the new target images. 

## What is your overall goal with this project?
The overall goal would be to train a pretrained yolo modeol to detect a very specific new target class. Once it can detect the new class we can use the bouding box's aspect ratio, overall size (x,y), and origin/center to detemine if the object has moved and/or changed orientation (ie. rotated).

## Anything else you want to note about your project?
Not exactly sure on the best way to automate the image labeling if it is even possible. Seems we wouldnt need image recognintion AI if this was easier.
