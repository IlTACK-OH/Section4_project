# <div align="center">🌎 ReadME</div>
<div align="center">
Roboflow의 Self Driving Car Image Dataset을 이용하여 YOLOv5 모델로 객체인식을 구현한 프로젝트입니다.

기본적으로 YOLOv5를 사용하여 만들어졌기 때문에 해당 공식 Repo 역시 참고바랍니다.

👉 [YOLOv5 공식Repo]


[YOLOv5 공식Repo]:https://github.com/ultralytics/yolov5
</div>


## 👀 Untitled1
- 모델을 실제로 구현할 때 사용한 colab파일입니다.
- 모델 구현과정을 확인할 수 있습니다.

## 👀 dist_ver
- 배포용 파일입니다.
- 간단하게 예측을 진행하고 싶은 파일이 있을 경우 해당 파일을 이용하면 됩니다.

## ❗ Dataset
- [다운로드 링크]

위의 링크를 통하여 Train, Valid, Test세트로 분할된 후 일정 수의 파일을 잘라낸 실제 프로젝트에서 사용한 파일을 다운로드 할 수 있습니다.

[다운로드 링크]:https://drive.google.com/file/d/1WStE4VCBXcyM8lxh13dZ4_MddhK_l0v5/view?usp=share_link

## 예측 클래스(총 11개)
- 'biker'
- 'car' 
- 'pedestrian'
- 'trafficLight'
- 'trafficLight-Green'
- 'trafficLight-GreenLeft'
- 'trafficLight-Red'
- 'trafficLight-RedLeft'
- 'trafficLight-Yellow'
- 'trafficLight-YellowLeft'
- 'truck'

## 모델 구조도
![172404576-c260dcf9-76bb-4bc8-b6a9-f2d987792583](https://user-images.githubusercontent.com/113511013/217157293-dd93d93c-49b2-4361-b2af-c4aa02965ab2.png)

## 모델 예측 모습
![test1](https://user-images.githubusercontent.com/113511013/217156038-8b209a7f-c57b-49fd-810a-804cf926cf55.jpg)

## 한계점 및 개선사항
제한된 메모리와 GPU할당량에서 진행하다보니 충분한 크기의 구한 데이터세트 전부를 사용하지 못하였습니다.

그러다 보니 데이터세트의 분할 문제로 인하여 자동차를 제외한 클래스에 대한 데이터가 부족해 다른 클래스에 대한 예측 정확도가 매우 낮습니다.

그리고 위의 문제점의 원인과 동일한 이유로 YOLOv5에서도 가벼운 모델인 YOLOv5s버전을 사용하다보니 정확도가 더욱 떨어진 것 같습니다.

또한 한국이 아닌 외국의 도로 사진을 이용하여 신호등의 체계가 다른 것 같습니다. 따라서 한국 도로에서 신호등을 잘 인식하지 못하는 문제 역시 파악했습니다.

이는 데이터세트의 추가적인 확보와 Colab Pro등을 이용하여 해결할 수 있는 부분으로 보입니다.

추후 다시 이 프로젝트를 손 볼 여유시간이 생기면 업데이트하도록 하겠습니다.

그리고 여러 모델을 이용하여 속도와 정확도를 직접 측정해보고 싶었지만, 그 부분을 실행해보지 못한 점이 아쉬움으로 남습니다.
