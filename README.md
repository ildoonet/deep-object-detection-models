# deep-object-detection-models
Deep Learning으로 학습된 Object Detection Model 에 대해 정리한 Archive 임.

## 1편

Deep Learning 기반의 모델링으로 Object Detection 문제를 효과적으로 풀기위해 시도되었던 다양한 내용들을 정리한 자료입니다.

![Summary SlideShare #1](/object-detection-1.png?raw=true "Summary")

**[1편 SlideShare](https://www.slideshare.net/IldooKim/deep-object-detectors-1-20166)**


### R-CNN 이전의 모델

* DPM : [Object Detection with Discriminatively TrainedPart Based Models](http://cs.brown.edu/~pff/papers/lsvm-pami.pdf)
* [Selective Search for Object Recognition](http://cs.brown.edu/~pff/papers/lsvm-pami.pdf)
* [OverFeat: Integrated Recognition, Localization and Detection using Convolutional Networks](https://arxiv.org/abs/1312.6229)
* [Deep Neural Networks for Object Detection](https://pdfs.semanticscholar.org/713f/73ce5c3013d9fb796c21b981dc6629af0bd5.pdf)

### R-CNN 류의 모델 : R-CNN의 모듈들을 개선했거나 유사 구조의 Detection Pipeline을 사용 

* R-CNN : [Rich feature hierarchies for accurate object detection and semantic segmentation](https://arxiv.org/abs/1311.2524)
  * [Spatial Pyramid Pooling in Deep Convolutional Networks for Visual Recognition](https://arxiv.org/abs/1406.4729) : 이미지를 
  반복해서 Crop해 DNN Feature를 얻는 과정을 개선하기 위해 SPP Layer소개.
  * [Object detection via a multi-region & semantic segmentation-aware CNN model](http://arxiv.org/abs/1505.01749) : Feature Level  
  RNN으로 Context Feature Extract하여 Concat
* [Fast R-CNN](https://arxiv.org/abs/1504.08083) : R-CNN의 파이프라인에서 마지막 부분에 해당하는 SVM을 Neural Network로 개선해 성능과 속도를 높임.
* [Faster R-CNN](http://arxiv.org/abs/1506.01497) : R-CNN의 파이프라인에서 첫번쨰 부분에 해당하는 Selective Search(Proposal)을 Neural Network로 개선해 속도와 성능 개선함.
  * [R-CNN Minus R](http://arxiv.org/abs/1506.06981)
  * [G-CNN: an Iterative Grid Based Object Detector](http://arxiv.org/abs/1512.07729)
  * [Faster R-CNN +++](https://arxiv.org/abs/1512.03385)
* [R-FCN: Object Detection via Region-based Fully Convolutional Networks](https://arxiv.org/abs/1605.06409) : Faster R-CNN을 Fully Convolutional 하게 변경.

### Single Shot Detector : 1번의 Neural Network Forwarding으로 여러 클래스의 여러 물체를 동시 검출하는 Pipeline을 사용

* Multibox, Edgebox, MSC-Multibox 등 DNN 기반의 방식으로 Proposal 개선하기도 함.
  * [Scalable Object Detection using Deep Neural Networks](https://arxiv.org/abs/1312.2249)
  * [Edge Boxes: Locating Object Proposals from Edges](http://research.microsoft.com/pubs/220569/ZitnickDollarECCV14edgeBoxes.pdf)
  * [Scalable, High-Quality Object Detection](http://arxiv.org/abs/1412.1441)
  * [DeepBox: Learning Objectness With Convolutional Networks](https://github.com/weichengkuo/DeepBox)
* [You Only Look Once: Unified, Real-Time Object Detection](http://arxiv.org/abs/1506.02640)
  * Overfeat, Multibox 등의 Formulation을 발전시키고, Network Architecture의 개선으로 성능 개선
* [SSD: Single Shot MultiBox Detector](http://arxiv.org/abs/1512.02325)
  * Faster RCNN 등과 성능이 비등하면서도 YOLO만큼 빠름

----
