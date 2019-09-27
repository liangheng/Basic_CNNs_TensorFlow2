# Basic_CNNs_TensorFlow2
A tensorflow2 implementation of some basic CNNs.

## Networks included:
+ MobileNet_V1
+ MobileNet_V2
+ [MobileNet_V3](https://github.com/calmisential/MobileNetV3_TensorFlow2)

## Other networks
For AlexNet and VGG, see : https://github.com/calmisential/TensorFlow2.0_Image_Classification<br/>
For InceptionV3, see : https://github.com/calmisential/TensorFlow2.0_InceptionV3<br/>
For ResNet, see : https://github.com/calmisential/TensorFlow2.0_ResNet

## Train
1. Requirements:
+ Python >= 3.6
+ Tensorflow >= 2.0.0-rc2
2. To train the ResNet on your own dataset, you can put the dataset under the folder **original dataset**, and the directory should look like this:
```
|——original dataset
   |——class_name_0
   |——class_name_1
   |——class_name_2
   |——class_name_3
```
3. Run the script **split_dataset.py** to split the raw dataset into train set, valid set and test set. The dataset directory will be like this:
 ```
|——dataset
   |——train
        |——class_name_1
        |——class_name_2
        ......
        |——class_name_n
   |——valid
        |——class_name_1
        |——class_name_2
        ......
        |——class_name_n
   |—-test
        |——class_name_1
        |——class_name_2
        ......
        |——class_name_n
```
4. Run **to_tfrecord.py** to generate tfrecord files.
5. Change the corresponding parameters in **config.py**.
6. Run **train.py** to start training.
## Evaluate
Run **evaluate.py** to evaluate the model's performance on the test dataset.

## References
1. MobileNet_V1: [Efficient Convolutional Neural Networks for Mobile Vision Applications](https://arxiv.org/abs/1704.04861)
2. MobileNet_V2: [Inverted Residuals and Linear Bottlenecks](https://arxiv.org/abs/1801.04381)
3. MobileNet_V3: [Searching for MobileNetV3](https://arxiv.org/abs/1905.02244)
