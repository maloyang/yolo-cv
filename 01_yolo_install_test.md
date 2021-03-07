# yolo install, test (2021-01-23)

## 參考文
- https://www.codenong.com/cs106180350/
- https://github.com/qqwweee/keras-yolo3

## 安裝
- 用conda安裝
- `conda create -n py36 python=3.6` 使用python3的環境
- `conda activate py36` 啟用
- `pip install yolov3` 沒想到這樣就可以安裝完!
- `D:\python\yolo\keras-yolo3-master>python convert.py yolov3.cfg yolov3.weights model_data/yolo.h5`
- `python yolo_video.py --image` 這樣就可以開始辨識
    - 不過要先安裝: `pip install matplotlib`

