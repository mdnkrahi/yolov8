## Install YOLOv8 Inside Docker Container

### Run Docker image

Run command to create Docker image:
```sh docker build -t yolov8 .```


### Testing YOLOv8

Create directory to store input images:
```mkdir -p ~/yolov8/inputs```

Download sample image:
```curl -o ~/yolov8/inputs/test.jpg https://raw.githubusercontent.com/rdcolema/tensorflow-image-classification/master/cat.jpg```