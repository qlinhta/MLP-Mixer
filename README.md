Implementation for paper [MLP-Mixer: An all-MLP Architecture for Vision](https://arxiv.org/pdf/2105.01601.pdf)

<img src="/home/qlinhta/mlp-mixer/images/architecture.PNG" width="500"/>

### Set up your dataset.

Create 2 folders `train` and `validation` in the `data` folder (which was created already). Then `Please copy` your images with the corresponding names into these folders.

- `train` folder was used for the training process
- `validation` folder was used for validating training result after each epoch 

This library use `image_dataset_from_directory` API from `Tensorflow 2.0` to load images.

### Train your model

```bash
python train.py --epochs ${epochs} --num-classes ${num_classes}
```

```bash
python train.py --epochs 10 --num-classes 2
```
### Testing model

```bash
python predict.py --test-file-path ${test_file_path}
```

where `test_file_path` is the path of your test image.

Example:

```bash
python predict.py --test-file-path ./data/test/Image.jpg
```