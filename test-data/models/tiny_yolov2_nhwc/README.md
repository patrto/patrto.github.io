`.npy` files under this folder are downloaded from model of Tiny YOLO v2, which is converted from [YAD2K project](https://github.com/allanzelener/YAD2K) and  licensed under the MIT.

The test data are generated by running TinyYolov2 model based on [YAD2K project](https://github.com/BruceDai/YAD2K/tree/gen_test_data) with [yolov2-tiny-voc.cfg](https://raw.githubusercontent.com/pjreddie/darknet/master/cfg/yolov2-tiny-voc.cfg) and [yolov2-tiny-voc.weights](http://pjreddie.com/media/files/yolov2-tiny-voc.weights).

Details of test data: 

1. `input_0.npy` and `output_0.npy` of [test_data_set/0](test_data_set/0) is generated by running TinyYolov2 model with [dog.jpg](https://github.com/allanzelener/YAD2K/blob/master/images/dog.jpg) 
2. `input_0.npy` and `output_0.npy` of [test_data_set/1](test_data_set/1) is generated by running TinyYolov2 model with [horses.jpg](https://github.com/allanzelener/YAD2K/blob/master/images/horses.jpg) 
3. `input_0.npy` and `output_0.npy` of [test_data_set/2](test_data_set/2) is generated by running TinyYolov2 model with [person.jpg](https://github.com/allanzelener/YAD2K/blob/master/images/person.jpg) 

Commands to generate test data:

```sh
$ git clone https://github.com/BruceDai/YAD2K && cd YAD2K
$ git checkout gen_test_data
$ python3 test_yolo.py model_data/yolov2-tiny-voc.h5 -a model_data/yolov2-tiny-voc_anchors.txt -c model_data/pascal_classes.txt
```