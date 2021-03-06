# Computer Vision Guide
> These are some notes that i have accumulated throughout my projects. I believe that they would help a lot in my later projects. And i hope they would help you too
## YOLO architecture studying
### 1. How to train your own YOLO model
If you want to train your own YOLO, please check my project **Training_YOLOv4_tiny.ipynb**. Some notes before you can apply this file in your own project: 
- This file follows these three references: [AlexeyAB repository](https://github.com/AlexeyAB/darknet#how-to-train-to-detect-your-custom-objects) and [Roboflow guide how to YOLO model](https://blog.roboflow.com/how-to-train-yolov5-on-a-custom-dataset/), and [How to train your own model with crowd human dataset](https://github.com/jkjung-avt/yolov4_crowdhuman)
- I stuck for days to figure out how to configure the right GPU architecture in Makefile. [Roboflow guide how to YOLO model](https://blog.roboflow.com/how-to-train-yolov5-on-a-custom-dataset/), [How to train your own model with crowd human dataset](https://github.com/jkjung-avt/yolov4_crowdhuman) help me alot. If you want to customize to train your own model, you must understand your GPU architecture. My comments in the project may help you.
- If you get stuck in how to prepare files (especially train.txt and test.txt files) I've supported you with a section which helps creating these two files. Remember to modify your dataset ratio!
- Another tips you can try is that you can prepare 3 files, 'train.txt', 'test.txt', 'validation.txt'. In your training process, you can configure .data file to make DarkNet use **train.txt** and **validation.txt** files. **Test.txt** is forbidden until you reach the end of training process. After that, you can configure Darknet to use your **Test.txt** file to make the best evaluation. 
- Before you jump into my colab notebook: Prepare a **yolov4-tiny** folder in your GG Drive first. my colab notebook will link to that folder and automatically link weights to that folder!

**Version 2**: I have another version named *Training_YOLOv4_tiny_Drive_based.ipynd* which will work on darknet framework contained by google drive. I don't know if this could affect your training performance. If yes, please let me know and try the original version in which you will have to make some manual adjustment but finally it will save weights to your drive too!
