## Introduction
Here is my python source code for QuickDraw - an online game developed by google. with my code, you could: 
Run an app which you could draw in front of a camera 


## Camera app
```
python mediapipe_app.py
```

## Demo
./demo

## Dataset
The dataset used for training my model could be found at [Quick Draw dataset] https://console.cloud.google.com/storage/browser/quickdraw_dataset/sketchrnn. 
Here I only picked up 20 files for 20 categories.
You need to download them into ./data

## Categories:
The table below shows 20 categories my model used:

|           |           |           |           |
|-----------|:-----------:|:-----------:|:-----------:|
|   apple   |   book    |   bowtie  |   candle  |
|   cloud   |    cup    |   door    | envelope  |
|eyeglasses |  guitar   |   hammer  |    hat    |
| ice cream |   leaf    | scissors  |   star    |
|  t-shirt  |   pants   | lightning |    tree   |

## Training

You need to download npz files corresponding to 20 classes my model used and store them in folder **data**. If you want to train your model with different list of categories, you only need to change the constant **CLASSES** at **src/config.py** and download necessary npz files. Then you could simply run:
```
python train.py
```

## Requirements

* **python 3.6**
* **cv2**
* **pytorch** 
* **numpy**
