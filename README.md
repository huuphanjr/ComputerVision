# YOLOv5s-based Self-Checkout Fruit Detection System


# Installation guide

## Step 1: Set Up the YOLOv5s environment

Installing the necessary dependencies as outlined in our repository's README. Clone the YOLOv5 repository to your local machine by following the provided instructions.

## Step 2: Prepare annotations in YOLOv5s-compatible format

Convert your annotations, regardless of their initial format (e.g., Pascal VOC, COCO), into the YOLOv5s-compatible format. Utilize the labelimg2yolo.py script available in our repository under the relevant directory. If your annotations are in a different format, adapt the script accordingly.

## Step 3: Define data configuration

Create a YAML file (e.g., data.yaml) within the repository's data folder. Inside this file, specify the paths leading to the training and validation image folders. Ensure to include the total count of fruit classes present in your dataset.

## Step 4: Initiate training of the fruit detection model

Access the **train.py** script located in the root directory of our YOLOv5s repository. Customize the training settings like model architecture, batch size, and learning rate. You can modify the script's arguments or use the command line for this purpose. Commence training by executing the following command:

**python train.py --data data/data.yaml --cfg models/yolov5s.yaml --weights '' --batch-size 8**


## Step 5: Monitor and Evaluate Training

While training, observe the progress and metrics displayed in the console. To evaluate the trained model's performance on the validation dataset, use the **val.py** script:

**python val.py --data data/data.yaml --weights path/to/best/weights.pt**





