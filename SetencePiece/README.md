# Naver Movie Review Classification
네이버 영화 리뷰 데이터를 대상으로 여러 토크나이저를 적용해보는 프로젝트 입니다. 해당 프로젝트에 대한 블로그는 [여기](https://vg-rlo.tistory.com/entry/Classification-Naver-Movie-Review-Sentiment-Classification-Using-Setencepiece?category=452346)로 들어가면 보실 수 있습니다. 

## Text Preprocessing using Tokenizer
* Setencepiece
* Mecab in Konlpy

## 오픈 데이터셋 다운로드 
* [Korean parallel corpora](https://github.com/jungyeul/korean-parallel-corpora)
```
$ wget https://github.com/jungyeul/korean-parallel-corpora/raw/master/korean-english-news-v1/korean-english-park.train.tar.gz
```
```
$ mkdir -p ~/aiffel/sp_tokenizer/data
```
```
$ mv korean-english-park.train.tar.gz ~/aiffel/sp_tokenizer/data
```
```
$ cd ~/aiffel/sp_tokenizer/data
```
```
$ tar -xzvf korean-english-park.train.tar.gz
```
## 설치 라이브러리  
* [sentencepiece](https://github.com/google/sentencepiece): Google에서 제공하는 오픈소스 기반 Sentence tokenizer/detokenizer
* [konlpy](https://konlpy.org/ko/latest/install/)

### Konlpy 설치 
```
$ sudo apt-get install g++ openjdk-8-jdk
```

```
$ bash <(curl -s https://raw.githubusercontent.com/konlpy/konlpy/master/scripts/mecab.sh)
```

```
$ pip install konlpy
```

## 프로젝트 결과 
* SentencePiece를 사용하여 Corpus, preprocessing, Sentence piece 적용, tokenizer 구현 및 동작이 정상적으로 진행됐는지 
* SentencePiece를 통해 만든 tokenizer가 text classification 모델로 정상적으로 수렴하여 80% 이상의 test accuracy를 냈는지
* Sentencepiece와 다른 tokenizer와 성능 비교 

|model|vocab_size|tokenizer|loss   |accuracy|
|-----|----------|---------|-------|--------|
|LSTM|8000|Sentencepiece/model_type=unigram|0.4477|0.8172|
|GMP|8000|Sentencepiece/model_type=unigram|0.4118|0.8149|
|LSTM|8000|Mecab|0.4127|0.8274|
|GMP|8000|Mecab|0.3812|0.8280|
