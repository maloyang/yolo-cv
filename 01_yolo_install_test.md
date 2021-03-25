# yolo install, test (2021-01-23)

## 參考文
- https://www.codenong.com/cs106180350/
- https://github.com/qqwweee/keras-yolo3

## 安裝
- 用conda安裝
- `conda create -n py36 python=3.6` 使用python3的環境
- `conda activate py36` 啟用
- `pip install yolov3` 沒想到這樣就可以安裝完!
- 下載人家訓練好的
  - `git clone https://github.com/qqwweee/keras-yolo3`
  - `cd keras-yolo3`
  - 這是yolo原始提供訓練過的
  - `wget https://pjreddie.com/media/files/yolov3.weights`
  - `python convert.py yolov3.cfg yolov3.weights model_data/yolo.h5`
  - 做上面的動作時可能會出錯 "ImportError: `save_model` requires h5py."，可以下指令
  - `pip uninstall h5py`
- `python yolo_video.py --image` 這樣就可以開始辨識，但是會報錯"ModuleNotFoundError: No module named 'PIL'"
    - 先安裝: `pip install Pillow, matplotlib`
- 這時在win10以可以跑，但是ubuntu20.04上還是GG
  - `pip install 'h5py==2.10.0' --force-reinstall` --> 改變h5py就可以了
  - 

## 測試影片
- python yolo_video.py --input videos/traffic.mp4 --output videos/traffic_p.mp4
- 不帶`--output`參數就不會輸出影片結果
