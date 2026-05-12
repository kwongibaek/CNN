# CNN
CNN (Convolutional Neural Network)

: Convolutional 계산을 통해 시각적 영상을 분석하는 데 사용되는 다층의 feed-foward neural network

주의! input의 첫번째 차원은 배치차원 (유지 필요!)

-Convolutional layer

: 기존의 muti 퍼셉트론과 달리 fully connected되어 있지 않고 filter를 통해 합성곱 연산을 진행하는 layer

+filter: 모든 입력 채널을 커버하는 kernal의 묶음

(filter의 개수만큼 feature map 존재)

입력에 곱해지는 가중치 => kernal

(입력 채널 수 = kernal 수)

합성곱 연산을 통해 얻은 출력 => feature map 

점차 깊이가 깊어지고 너비와 높이는 낮아짐 

+패딩 (padding)

: 입력 배열의 주위를 0으로 채우는 것 

type1. same padding : 입력과 feature map의 크기를 동일하게 만드는 경우

type2. valid padding: 패딩 없이 순수한 입력 배열에서만 합성곱하는 경우

--> 중앙부와 모서리의 합성곱에 참여하는 비율이 달라지기에 주로 same을 사용

+ 스트라이드 (Stride)

: kernal의 이동의 크기 

(기본이 1 == 1칸씩 움직임)

- Pooling layer

: feature map의 공간적인 특성은 유지하면서 크기를 줄이는 역할 수행 

-->stride를 크게 하는 것보다 더 나은 성능을 보이기에 

--> 개수는 변화지 않음

--> 겹치는 부분 존재X

type1. max pooling

--> MaxPooling2D()

=> maxpooling을 자주 사용

type2. average pooling

-->AveragePooling2D()

- Flattening layer

: Fully connected layer에 연결하여 분류를 하기 위해 필요
