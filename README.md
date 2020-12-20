# tflite_object_detection
## AI inference using TF Lite on Raspberry Pi 4

**Configuration:**
python -m pip install virtualenv  
python -m venv tflite-env  
source tflite-env/bin/activate  

sudo apt -y install libjpeg-dev libtiff5-dev libjasper-dev libpng12-dev libavcodec-dev libavformat-dev libswscale-dev libv4l-dev libxvidcore-dev libx264-dev

python -m pip install opencv-contrib-python==4.1.0.25

goto website: tensorflow.org/lite/guide/python  
wget https://storage.googleapis.com/download.tensorflow.org/models/tflite/coco_ssd_mobilenet_v1_1.0_quant_2018_06_29.zip


**Download Model and Labels:**  
mkdir coco_ssd_mobilenet_v1  
unzip coco_ssd_mobilenet_v1_1.0_quant_2018_06_29.zip -d coco_ssd_mobilenet_v1  

**Use netron to preview model details:**  
pip3 install netron

**Based on:**  
https://github.com/EdjeElectronics  
https://www.digikey.pl/en/maker/projects/how-to-perform-object-detection-with-tensorflow-lite-on-raspberry-pi/b929e1519c7c43d5b2c6f89984883588

**Start recognition from video stream:**\
source tflite-env/bin/activate\
python TFLite_detection_webcam.py --modeldir=object_detection/coco_ssd_mobilenet_v1
