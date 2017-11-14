# Mask RCNN
Mask RCNN in TensorFlow

这个项目试图去重新实现由Kaiming He等人提出的惊人的构想：
[Mask R-CNN](https://arxiv.org/abs/1703.06870)

##环境要求

原先的环境要求：
- [Tensorflow (>= 1.0)](https://www.tensorflow.org/install/install_linux)
- [Numpy](https://github.com/numpy/numpy/blob/master/INSTALL.rst.txt)
- [COCO dataset](http://mscoco.org/dataset/#download)
- [Resnet50](http://download.tensorflow.org/models/resnet_v1_50_2016_08_28.tar.gz)

我的运行环境
- 操作系统：Windows 10
- Python 3.6.3
- Tensorflow 1.4.0

## 如何执行
1. 进入 `./libs/datasets/pycocotools`文件夹然后运行 `make`
2. 下载 [COCO](http://mscoco.org/dataset/#download) 的数据集, 把它们放在 `./data`中, 然后执行 `python download_and_convert_data.py` 建立 tf-records. 这一条将会花费好长一段时间.
3. 下载预训练的 resnet50 模型, `wget http://download.tensorflow.org/models/resnet_v1_50_2016_08_28.tar.gz`, 把它解压完后放到`./data/pretrained_models/`里面
4. 进入 `./libs` 执行 `make`
5. 执行 `python train/train.py` 开始训练
6. 这里可能还是会有很多很多的Bug，欢迎大家一起来修正它们

## 目标:
- [x] ROIAlign
- [x] COCO Data Provider
- [x] Resnet50
- [x] Feature Pyramid Network
- [x] Anchor and ROI layer
- [x] Mask layer
- [x] Speedup anchor layer with cython
- [x] Combining all modules together.
- [x] Testing and debugging (in progress)
- [ ] Training / evaluation on COCO
- [ ] Add image summary to show some results
- [ ] Converting ResneXt
- [ ] Training >2 images

## 欢迎大家贡献自己的一份力量
- 大家可以先移步原作者的仓库里面进行编辑
- 此处的代码仅做为测试
- Anything helps this repo, including **discussion**, **testing**, **promotion** and of course **your awesome code**.

## 万分感谢
此项目从下面借鉴了很多的代码
- [TFFRCNN](https://github.com/CharlesShang/TFFRCNN)
- [py-faster-rcnn](https://github.com/rbgirshick/py-faster-rcnn)
- [faster_rcnn](https://github.com/ShaoqingRen/faster_rcnn)
- [tf-models](https://github.com/tensorflow/models)

## License
在 [LICENSE](https://github.com/CharlesShang/FastMaskRCNN/blob/master/LICENSE) 查看更多信息.

