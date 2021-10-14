# YOLOV5 Mask Detection
Detection API Deployed via Flask

<details open>
<summary>Inference</summary>

`detect.py` runs inference on a variety of sources, downloading models automatically from
the [latest YOLOv5 release](https://github.com/ultralytics/yolov5/releases) and saving results to `runs/detect`.

```bash
$ python detect.py --source 0  # webcam
                            file.jpg  # image 
                            file.mp4  # video
                            path/  # directory
                            path/*.jpg  # glob
                            'https://youtu.be/NUsoVlDFqZg'  # YouTube video
                            'rtsp://example.com/media.mp4'  # RTSP, RTMP, HTTP stream
```

</details>

<details open>
<summary>Training</summary>

Run commands below to resume training
on mask dataset (dataset auto-downloads on
first use). Training times for YOLOv5s are 10 hours on a GTX1060TI (multi-GPU times faster). 
  
```bash
$ python train.py --resume
```

<img width="800" src="https://github.com/Zhenyu2077/YOLOV5_Mask_Detection/blob/main/runs/train/exp3/results.png?raw=trueg">
<img width="800" src="https://raw.githubusercontent.com/Zhenyu2077/YOLOV5_Mask_Detection/main/runs/train/exp3/test_batch1_pred.jpg">
</details>

<details open>
<summary>Web API</summary>

Implement the API via flask of custom model weight.
API consisting of a form where you can upload an image, and see the inference result of the model in the browser.

```bash
$ python3 webapp.py --port 5000
```
  
 <p align="center">
<img src="https://github.com/Zhenyu2077/YOLOV5_Mask_Detection/blob/main/Screenshot_Web.png" width="600">
  </p>
 <p align="center">

<img width="400" src="https://github.com/Zhenyu2077/YOLOV5_Mask_Detection/blob/main/test.jpg">
<img width="400" src="https://github.com/Zhenyu2077/YOLOV5_Mask_Detection/blob/main/image0.jpg">
  </p>
</details>
