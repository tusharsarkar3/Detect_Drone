<div align="center">
<p>
<img width="850" src="ss/cover.jpg"></a>
</p>
<br>
<p>
 This drone detection system uses YOLOv5 which is a family of object detection architectures and we have trained the model on <a href="https://www.kaggle.com/dasmehdixtr/drone-dataset-uav">Drone Dataset</a>.
</p>

</div>


## <div align="center">Overview</div>


<details open>
<summary>Install</summary>

Python >= 3.6.0 required with all [requirements.txt](https://github.com/tusharsarkar3/Detect_Drone/blob/main/requirements.txt) dependencies installed:
```bash
$ git clone https://github.com/tusharsarkar3/Detect_Drone.git
$ pip install -r requirements.txt
```
 
</details>

<details>
<summary>Training</summary>

 The structure of the file system is of great importance here so these images will show you the correct way of organizing it. The main folder named datasets should be on the same level as this repository. The next steps are elaborated in the images: 
 
 1. The two folders with images and labels respectively should be inside the dataset folder.
 <img width="800" src="ss/img2.png">
 
 2. The images directory should contain the training images and the validation images respectively.
 <img width="800" src="ss/img3.png">

 3. The labels directory should contain the training labels and the validation labels respectively.
 <img width="800" src="ss/img4.png">
 
Run commands below to reproduce results on [Drone Dataset](https://www.kaggle.com/dasmehdixtr/drone-dataset-uav) dataset..
```bash
$ $ python train.py --img 640 --batch 16 --epochs 15 --data coco128.yaml --weights yolov5s.pt

```

 Check out <a href="https://github.com/ultralytics/yolov5">YOLOv5</a> for more information.
</details>  

<details open>
<summary>Inference </summary>

```bash
$ python detect.py --weights 'path to the best set of weights' --source 0  # webcam       
                                                                        file.jpg  # image 
                                                                        file.mp4  # video
                                                                        path/  # directory
                                                                        path/*.jpg  # glob
                                                                        'https://youtu.be/NUsoVlDFqZg'  # YouTube video
                                                                        'rtsp://example.com/media.mp4'  # RTSP, RTMP, HTTP stream
```
 The results will be stored in a new directory named run which will be on the same level as the root directory.
 
 Check out <a href="https://github.com/ultralytics/yolov5">YOLOv5</a> for more information.
</details>



---
### Results:

![img](exp27/test_batch0_pred.jpg)
![img](exp27/results.png)
![img](exp27/P_curve.png) 
![img](exp27/R_curve.png)
![img](exp27/PR_curve.png)

---

<h3 align="center"><b>Developed with :heart: by <a href="https://github.com/tusharsarkar3">Tushar Sarkar</a>
