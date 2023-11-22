# Install YOLOv8 Inside Docker Container

## Run Docker image

Run command to create Docker image:
```sh 
docker build -t yolov8 .
```


## Testing YOLOv8

### Create directory to store input images:
```sh 
mkdir -p ~/yolov8/inputs 
```

### Download sample image:
```sh
 curl -o ~/yolov8/inputs/test.jpg https://raw.githubusercontent.com/rdcolema/tensorflow-image-classification/master/cat.jpg 
 ```

## Run the following commands in YOLOv8 container to perform required task:

### 1. Object detection:
```sh
docker run -it --rm \
    -v ~/yolov8:/yolov8 \
    yolov8 detect predict save model=yolov8s.pt source=inputs/test.jpg
 ```
 Output directory: ```~/yolov8/runs/detect.```

### 2. Image segmentation:
```sh
 docker run -it --rm \
    -v ~/yolov8:/yolov8 \
    yolov8 segment predict save model=yolov8s-seg.pt source=inputs/test.jpg
 ```
 Output directory: ```~/yolov8/runs/segment.```

### 3. Image classification:
```sh
docker run -it --rm \
    -v ~/yolov8:/yolov8 \
    yolov8 classify predict save model=yolov8s-cls.pt source=inputs/test.jpg
 ```
 Output directory: ```~/yolov8/runs/classify.```

 ## Remove Docker image
  ### To remove YOLOv8 image, run the following command:
```sh
 docker rmi yolov8
 ```
