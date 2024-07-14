# Object Detection using Custom Dataset with YOLOv8: Detecting Football Players and Footballs
Welcome to this tutorial on object detection using a custom dataset with YOLOv8. In this tutorial, we will introduce YOLOv8, Google Open Image V7, and the process of annotating images using CVAT.ai. We will also cover how to take our own photographs, annotate them, create the necessary image and label folders, and train the model using Google Colab. Finally, we'll use OpenCV to process a video and detect football players and footballs.

## Step 1
Google Open Image V7 is a  great service that provides over 9M annotated images for object detection with over 600 classes. You can use tools like the Open Images Downloader or scripts provided by the Open Images dataset repository.
![image](https://github.com/user-attachments/assets/25448c3d-3b4d-48fa-8bf7-5297929dac7b)

### Using Open Images Downloader
Install OVID6

```bash
pip install openimages
```
```bash
openimages downloader --data_dir ./data --class_names "Football","Person"
```
Replace "Football","Person" with the classes you are interested in. This command will download images of soccer balls and people.

## Step 2
Now we can annotate the images using cvat.ai 
![image](https://github.com/user-attachments/assets/4de3071a-a183-42a9-974f-9c3b8b0bb0e5)

first create account and sign up
1. Then create a new task
2. Fill in the task details such as task name, labels, etc.
3. In the "Files" section, click "Upload" and select the images you downloaded from Open Image V7.
4. Use the annotation tools provided by CVAT.ai to draw bounding boxes around football players and footballs. Assign the correct labels to each bounding box.

5. After you have annotated all the images, you can export the annotations in the format needed for training your YOLOv8 model.
6. Choose the "YOLO" format to export annotations in a format compatible with YOLO models.

## Step 3
1. Go to Google Drive and Create a New Folder for your Project
2. Create a sub folder called data
3. Create a two subfolders images and labels
4. Create another two subfolders called train and val in both images and labels forlder
5. Upload 80% of the images to images/train and 20% to images/val
6. Upload 80% of the annotations to labels/train and 20% to labels/val

## Step 4
1. Copy config.yaml to the root folder
2. Copy train.ipynb to the root folder
3. Execute train.ipynb

## Step 5 
1. Create a subfolder called video on root directory
2. Upload the Input video to video /folder
3. copy object_detection.ipynb to root folder and execute
4. Output video will be saved /video folder
