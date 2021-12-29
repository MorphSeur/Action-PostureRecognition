# Human Action Classification
Pose estimation & detection has been minimally implemented using the OpenPose implementation https://github.com/ildoonet/tf-pose-estimation with Tensorflow. For binary classification of poses, (sitting or upright), MobileNet (a CNN originally trained on the ImageNet Large Visual Recognition Challenge dataset), was retrained (final layer) on a dataset of ~1500 images of poses.
For classifying scenes around the person in consideration, we retrain Inception-v3 architecture on the Stanford 40 dataset (9523 images), which incorporates 40 different day-to-day activites. 

Pose classification accuracy is 94.56% and scene recognition rate is 92.3%. 

Check [README.md](https://github.com/MorphSeur/Action&PostureRecognition/tree/master/archive/README.md) located in archive for more details.

## Labels
Sitting and upright.

## Requirements
Please refer to [requirements.txt](https://github.com/MorphSeur/Action&PostureRecognition/blob/master/requirements.txt).

## Python scripts
### Pose Estimation and Action Classification on a Single Image
```
$ python3 run_image.py --image=1.jpg
```

Also, please do not forget to change the `address` variable in the code according to your local machine. This is a TODO, in the sense that the viewer can use `os.getcwd()` for an improved generic performance.

### Pose Estimation and Action Classification on Webcam

```
$ python3 run_webcam.py
```

## Issues
Insufficient number of labels.