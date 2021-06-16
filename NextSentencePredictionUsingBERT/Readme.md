# Model

* 사용 모델: Pretrained BERT



# Data Download 

* 사용 데이터셋: Kowiki 

```python
$ mkdir -p ~/aiffel/bert_pretrain/data
$ mkdir -p ~/aiffel/bert_pretrain/models
$ wget https://aiffelstaticprd.blob.core.windows.net/media/documents/kowiki.txt.zip
$ mv kowiki.txt.zip ~/aiffel/bert_pretrain/data
$ cd ~/aiffel/bert_pretrain/data && unzip kowiki.txt.zip
```



# Install Library 

```python
$ pip install sentencepiece # 토크나이저
$ pip install tqdm # 소요시간 확인
```

