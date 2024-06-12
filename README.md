# Train-yolov8-object-detection
Train yolov8 on object detection for detecting football players

## 📚 Dataset
The dataset is from RoboFlow.
There are 4 classes: Ball, Referee, Football Players, and Goalkeepers 
The format and annotation used is YoloV8.
RoboFlow
```
@misc{
football-players-detection-3zvbc_dataset,
title = { football-players-detection Dataset },
type = { Open Source Dataset },
author = { Roboflow },
howpublished = { \url{ https://universe.roboflow.com/roboflow-jvuqo/football-players-detection-3zvbc } },
url = { https://universe.roboflow.com/roboflow-jvuqo/football-players-detection-3zvbc },
journal = { Roboflow Universe },
publisher = { Roboflow },
year = { 2024 },
month = { may },
note = { visited on 2024-06-12 },
}
```

## 💯 Results
Sample Prediction of the test images:
![test image 1](https://github.com/sleepreap/train-yolov8-object-detection/assets/98008874/3174e1e8-fb59-4a54-9bd2-cf72e8f15530)
![test image 2](https://github.com/sleepreap/train-yolov8-object-detection/assets/98008874/fd522d60-93d5-44fb-9a8a-5fb31f6b4fc9)
![test image 3](https://github.com/sleepreap/train-yolov8-object-detection/assets/98008874/50ae90a1-c36f-48eb-8970-dddc7b44f69e)

Sample Prediction of the a video clip:
![ezgif-6-4a0f6c8918](https://github.com/sleepreap/train-yolov8-object-detection/assets/98008874/420ff9d4-0c6c-4643-ac91-bd9e1b986bd9)

Confusion Matrix of the prediction:
![confusion matrix](https://github.com/sleepreap/train-yolov8-object-detection/assets/98008874/82f2883e-38f4-4d7b-b697-54b5d6ee38c6)


## 🎯 Model Inference
To test out the model in real-time, you can upload images on the RoboFlow website where the model is hosted for real-time object detection. 
### [Model Inference: ](https://app.roboflow.com/yolov8-rmfc1/football-player-tracker-ghdyd/visualize/1)

## Hosted API
To run inference through Roboflow API using Python, use the roboflow Python package:
```
# import the inference-sdk
from inference_sdk import InferenceHTTPClient

# initialize the client
CLIENT = InferenceHTTPClient(
    api_url="https://detect.roboflow.com",
    api_key="API_KEY"
)

# infer on a local image
result = CLIENT.infer("YOUR_IMAGE.jpg", model_id="football-player-tracker-ghdyd/1")

```


