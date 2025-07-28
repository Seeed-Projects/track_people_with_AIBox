# Falldown detection

Using YOLOv8n for object detection and then determining whether two objects in consecutive frames are the same target by calculating the Intersection over Union (IoU) between them, thereby achieving the effect of object tracking.

## Hardware prepare

|                                               reCompuer AI Box                                              |                                               reComputer Industry AI Box                                               |
| :----------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------: |
| ![Raspberry Pi AI Kit](https://media-cdn.seeedstudio.com/media/catalog/product/cache/bb49d3ec4ee05b6f018e93f896b8a25d/i/m/image114993560.jpeg) | ![reComputer R1100](https://media-cdn.seeedstudio.com/media/catalog/product/cache/bb49d3ec4ee05b6f018e93f896b8a25d/2/-/2-114993595-recomputer-ai-industrial-r2135-12.jpg) |
| [**Purchase Now**](https://www.seeedstudio.com/reComputer-AI-R2130-12-p-6368.html?utm_source=PiAICourse&utm_medium=github&utm_campaign=Course) | [**Purchase Now**](https://www.seeedstudio.com/reComputer-AI-Industrial-R2135-12-p-6432.html?utm_source=PiAICourse&utm_medium=github&utm_campaign=Course) |

## Software prepare

### Install the runtime environment 

```bash
sudo apt update && sudo apt full-upgrade -y && sudo apt install hailo-all
```

### Install the project

```bash
git clone https://github.com/Seeed-Projects/track_people_with_AIBox.git
cd fall_detection_with_AIBox
```

### Prepare the python environment

```bash
python -m venv .env --system-site-packages  && source .env/bin/activate
pip install -r requirements.txt
```

## Run the project

```bash
python app.py -i ./people-walking.mp4 -n ./yolov8n.hef --show-fps -l ./common/coco.txt --track
```
## Result
[![Watch the video](https://img.youtube.com/vi/xoeMcaG_FxE/0.jpg)](https://www.youtube.com/watch?v=xoeMcaG_FxE)


## Reference

This project references  [Hailo-Application-Code-Examples](https://github.com/hailo-ai/Hailo-Application-Code-Examples).
