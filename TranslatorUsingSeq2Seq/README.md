# Translator Using Sequence to Sequence

## 디렉토리 셋팅
```
$ mkdir -p ~/aiffel/s2s_translation
```

## 설치 라이브러리 
```
$ sudo apt -qq -y install fonts-nanum
```

## 오픈 데이터셋 
* 제공처: [jungyeul github](https://github.com/jungyeul/korean-parallel-corpora/tree/master/korean-english-news-v1)
* 데이터명: korean-parallel-corpora     
  
## 사용 모델 
* Sequence to Sequence
    - Encoder: GRU
    - Decoder: GRU

## 프로젝트 결과 
* 번역기 모델 학습에 필요한 텍스트 데이터 전처리가 한국어 포함하여 잘 이루어졌다.
* 구두점, 대소문자, 띄어쓰기, 한글 형태소분석 등 번역기 모델에 요구되는 전처리가 정상적으로 진행되었다.
* Attentional Seq2seq 모델이 정상적으로 구동된다.
* seq2seq 모델 훈련 과정에서 training loss가 안정적으로 떨어지면서 학습이 진행됨이 확인되었다.
* 테스트 결과 의미가 통하는 수준의 번역문이 생성되었다.
* 테스트용 디코더 모델이 정상적으로 만들어져서, 정답과 어느 정도 유사한 영어 번역이 진행됨을 확인하였다.