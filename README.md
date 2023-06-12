# Implementasion of  deep learning -- Faster RCNN with GoogleNet as Backbone

## Overview
The data set used in this implementation is the Coco dataset, coco-2017. This implementation was created as an experiment to perform object tracking, specifically for people.

## Dependencies
Requires Python 3.10.11. Deep-learning Frameworks: [PyTorch](https://pytorch.org/).Basic Libraries: [NumPy](https://numpy.org/), [Matplotlib](https://matplotlib.org/), [Pandas](https://pandas.pydata.org/). Dataset : [Coco Dataset](https://cocodataset.org/#home), [FIFTYONE](https://docs.voxel51.com/index.html)

install fifty one
``` 
!pip install fiftyone
```
Download other dependencies 
```
!wget https://raw.githubusercontent.com/pytorch/vision/main/references/detection/transforms.py
!wget https://raw.githubusercontent.com/pytorch/vision/main/references/detection/engine.py
!wget https://raw.githubusercontent.com/pytorch/vision/main/references/detection/utils.py
!wget https://raw.githubusercontent.com/pytorch/vision/main/references/detection/coco_eval.py
!wget https://raw.githubusercontent.com/pytorch/vision/main/references/detection/coco_utils.py
```

## Parameter
Parameter use in bounding boxes, 
Anchorgenerator :
  - size : (32, 64, 128, 256, 512)
  - aspect ratio : (0.5, 1.0, 2.0)

Parameter use in Train :
  - Optimizer : SGD with lr = 0.005, momentum=0.9, weigth decay = 0.0005
  - Epoch : 10

## Result
Report when filter with confidence >0.75 :

![image](https://github.com/eyeshieldbat/indoai_person_tracking/assets/106160575/bbac3ca0-67e4-433b-8bac-67dd287954c2)

mAP : 0.19057

Precision-recall (PR) curves :

![image](https://github.com/eyeshieldbat/indoai_person_tracking/assets/106160575/e115cf26-2897-4c2c-8cde-dd3a34d09507)


Result sample prediction : 

![image](https://github.com/eyeshieldbat/indoai_person_tracking/assets/106160575/61849669-8e3f-4ae7-ace1-92893a6e59f4)

