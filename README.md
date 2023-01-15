# YOLO Hand Detection

YOLO (You Only Look Once) is a real-time object detection algorithm that is able to detect multiple objects within an image. The YOLO model divides the input image into a grid of cells, and for each cell, it predicts the probability of the presence of an object in that cell as well as the bounding box coordinates of the object. The YOLO algorithm is able to detect objects in real-time, in our case different hand gestures.

In order to accurately detect the number represented by a hand gesture, we trained two models. The first model used images from a web dataset called [roboflow](https://universe.roboflow.com/ktnf749-snu-ac-kr/sign-hb57g) that included ten different gestures, one for each number, and their position in each image. However, the model developed with these images had some inaccuracies with certain images. To improve performance, we trained a second model which included images of my own hands to the dataset. The comparison between the two models is shown in the next line (the top one is the basic model, the bottom one is the one with my hands included):

<div>
  <img src="https://raw.githubusercontent.com/JoseJuanRC/YOLO-HandDetection/main/Img/predict_model_1.png" alt="Model 1">
  <img src="https://raw.githubusercontent.com/JoseJuanRC/YOLO-HandDetection/main/Img/predict_model_2.png" alt="Model 2">
</div>

This comparison illustrates the improved performance of the second model, which correctly classifies all hand gestures except for the number two. To provide a clearer comparison, two gifs are presented, showing a video of both models in action. The top gif represents the basic model, while the bottom gif represents the model that includes my hands in the dataset.

![image1](https://raw.githubusercontent.com/JoseJuanRC/YOLO-HandDetection/main/output_base_img.gif)
![image1](https://raw.githubusercontent.com/JoseJuanRC/YOLO-HandDetection/main/output_myHands.gif)

In this case, we can observe that the first model has a high number of false detections and struggles to correctly classify some hand gestures. The second model, however, demonstrates a significant improvement with almost no false detections and accurate classification of all hand gestures, although it still presents some occasional errors.

To test the model, anyone can download the model weights at the following link:
- [Weights](https://alumnosulpgc-my.sharepoint.com/:f:/g/personal/jose_reyes119_alu_ulpgc_es/EvnDJH39opRBtTkCFI7NxDQBriaAHcjARowyger6KqjeUw?e=HgMHKB): 
  - best.pt: Basic model.
  - best_myHands.pt: Basic model + my hands.  
