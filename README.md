# YOLOV5 Mask Detection
Detection API Deployed via Flake 

<details open>
<summary>Inference</summary>

Inference with YOLOv5 and [PyTorch Hub](https://github.com/ultralytics/yolov5/issues/36). Models automatically download
from the [latest YOLOv5 release](https://github.com/ultralytics/yolov5/releases).

```python
import torch

# Model
model = torch.hub.load('ultralytics/yolov5', 'yolov5s')  # or yolov5m, yolov5l, yolov5x, custom

# Images
img = 'https://ultralytics.com/images/zidane.jpg'  # or file, Path, PIL, OpenCV, numpy, list

# Inference
results = model(img)

# Results
results.print()  # or .show(), .save(), .crop(), .pandas(), etc.
```

</details>



<details open>
<summary>Inference with detect.py</summary>

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

Implement the API via flack of custom model weight.
API consisting of a form where you can upload an image, and see the inference result of the model in the browser.

```bash
$ python3 webapp.py --port 5000
```
  
 <p align="center">
<img src="https://github.com/Zhenyu2077/YOLOV5_Mask_Detection/blob/main/Screenshot_Web.png" width="450">
  </p>
 <p align="center">

<img width="400" src="https://github.com/Zhenyu2077/YOLOV5_Mask_Detection/blob/main/test.jpg">
<img width="400" src="https://github.com/Zhenyu2077/YOLOV5_Mask_Detection/blob/main/image0.jpg">
  </p>
</details>
