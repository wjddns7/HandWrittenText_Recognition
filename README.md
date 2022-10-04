# 손글씨 인식 AI

## 1. 제작 기간
* 2일

## 2. 제작 도구
* OpenVINO

## 3. 핵심 기능
* 한글 및 영문 손글씨를 인식하고, 정확도를 높이는 것이 주 목적이다.

## 4. 설명
### (1) 국문의 경우 Binary로 구성된 손글씨 이미지를 Python코드를 이용해 이미지 파일로 변경 후, OpenVINO를 이용해 학습시킨다. 영문의 경우 기존 제공된 이미지를 활용하여 학습한다.
* 국문 손글씨 이미지
![image](https://user-images.githubusercontent.com/108790183/193737176-1b08c5db-cea0-4590-8e86-2cadceee5ec7.png)
13개 글자에 각 300~400개의 손글씨 데이터를 학습한다.<br/>
(용량이 커서 git에는 예시로 글자하나만 업로드하였다.)
* 영문 손글씨 이미지
![image](https://user-images.githubusercontent.com/108790183/193737348-162b5ab0-a101-4668-a212-bbecb90e9527.png)
### (2) 처음과 변경된 부분
*초기 기획은 한 단어를 인식하려 했으나, 급격한 난이도 상승으로, 낱자만 학습하여 인식할 수 있도록 변경. <br/>
![image](https://user-images.githubusercontent.com/108790183/193737849-a5e142c2-b6da-4414-871a-11d283085a55.png)
### (3) 구현 결과
* 국문 손글씨 이미지 4천개 이상 훈련한 모델의 결과는 아래와 같다. 영문 손글씨 이미지는 사전에 훈련되어 있어, 3개의 테스트 이미지를 이용했다.
* 국문 손글씨 결과 및 정확도
![image](https://user-images.githubusercontent.com/108790183/193738000-2bb71b06-8cdc-4f77-be81-fab259880ca4.png)
* 영문 손글씨 결과
![image](https://user-images.githubusercontent.com/108790183/193738103-22a98c33-a3bd-4cda-9b9a-93b90eb0838b.png)
### (4) 문제점
* 국문의 경우 학습시킨 이미지와 글씨체가 다르면 정확도가 떨어지며, 영문의 경우 테스트 이미지가 아닌 임의의 이미지를 사용하면 정확도가 떨어진다.
* 국문 이미지
![image](https://user-images.githubusercontent.com/108790183/193738244-b3069b2f-4a26-4eb0-ad17-8f6c34258d2a.png)
* 영문 이미지
![image](https://user-images.githubusercontent.com/108790183/193738285-4fe04034-84a1-45b8-ab75-e6b8cae47447.png)
## 5. 데이터 흐름도
![image](https://user-images.githubusercontent.com/108790183/193740337-e195e916-d6a8-4c95-b9c7-9ecb3f74ce17.png)

