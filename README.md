# AI based Web App - Image Labeling

- Vue based app
- OpenCV-JS for annotations and tracking
- ONNX, TensorFlow JS based helper functions

Object Tracking (Next frame object detection)
Objects localization
Segmentation
Resizing images

Import images
Export images + annotations (Pascal, COCO, other)

## Controls

* Moving selected bounding box  without modifying its size
```
    _____
____| ^ |____
| < | v | > |
```
* Modifying selected bounding box (CTRL for shrinking)
```
    _____              _____              
____| z |____      ____| w |____
| q | s | d |      | a | s | d |      
```
* Enter to get the next frame | GUI button

* Space to get the previous frame | GUI button

* Previous | Next ( if no bounding box is selected)
```
_____________
| < | v | > |
```
## Pros

* OS independant
* No installation required
* Better UI experience

## Cons

* Uploading all files might take time
* Longer inference time for helper functions

# Alternative

- Python 
- QT app
- OpenCV with TensorFlow/ONNX even PyTorch