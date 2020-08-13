# lidar-cone-classifier

This repository contains the codes used for training LiDAR Cone Classifier. The classifier performs classification on the images generated by `img_node` of the Ouster OS1-64 LiDAR. The LiDAR image crops have their intensity value capped at `1000` and rescaled to `[0, 255]`, then they are exported as `32 x 32` grayscale images.

## Dependencies

The list below contains some of the key dependencies required.

```
imgaug=0.4.0
pytorch=1.5.1
torchvision=0.6.1
pillow=7.2.0
matplotlib=3.3.0
numpy=1.19.1
```

## Folder Structure

It is assumed that the use has the folders setup as shown below.

```
├── data
│   ├── blue [578 entries exceeds filelimit, not opening dir]
│   └── yellow [500 entries exceeds filelimit, not opening dir]
├── README.md
└── train.ipynb
```

## Training and Inference

Currently all training and inference operations take place within the `train.ipynb` notebook.

## Todo

- [x] Implement basic pytorch image classifier
- [x] GPU checking and GPU training
- [x] Document dependencies and packages required to train the classifier.
- [ ] `pytorch-lightning` module to improve reproducibility and reduce boiler plate
- [ ] Export trained model to ONNX, so that it can be further optimised for TensorRT deployment.
- [ ] Investigate how to extend this to classify `oragne traffic cones`.