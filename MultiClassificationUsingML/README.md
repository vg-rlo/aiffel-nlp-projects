# News Category Multiclass Classification 

## 디렉토리 셋팅
```
$ mkdir -p ~/aiffel/reuters_classifiaction
```
    
## 오픈 데이터셋 
* 제공처: Tensorflow keras
* 데이터명: Reuters News(로이터 뉴스)     
     
## 사용 모델 
* Naive Bayes Classifier
* Complement Naive Bayes Classifier(CNB)
* Logistic Regression
* Support Vector Machine(SVM)
* Decision Tree 
* Random Forest
* GradientBoostingClassifier
* Voting
* MLP

## 프로젝트 결과 
* 3가지 단어 개수에 대해 8가지 머신러닝 기법을 적용하여 그 중 최적의 accuracy를 도출하였다.
* 파라미터를 조절해 분류 모델의 F1-score를 개선했다. 
* Vocabulary size에 따른 각 머신러닝 모델의 성능 변화 추이를 살피고, 해당 머신러닝 알고리즘의 특성에 근거해 원인을 분석하였다.
* 생성모델의 metric(BLEU 등)을 개선했다. 
* 동일한 데이터셋과 전처리 조건으로 딥러닝 모델의 성능과 비교하여 결과에 따른 원인을 분석하였다.

| Model                      |  vocab_size |  accuracy(%) | 
|----------------------------|-------------|--------------| 
| MultinomialNB              |  5000       |  67.32       | 
| MultinomialNB              |  10000      |  65.67       | 
| MultinomialNB              |  all        |  59.97       | 
| ComplementNB               |  5000       |  77.07       | 
| ComplementNB               |  10000      |  77.07       | 
| ComplementNB               |  all        |  76.49       | 
| LogisticRegression         |  5000       |  80.59       | 
| LogisticRegression         |  10000      |  80.77       | 
| LogisticRegression         |  all        |  81.34       | 
| SVC                        |  5000       |  80.81       | 
| SVC                        |  10000      |  80.50       | 
| SVC                        |  all        | 79.96        | 
| DecisionTreeClassifier     |  5000       |  61.98       | 
| DecisionTreeClassifier     |  10000      |  62.20       | 
| DecisionTreeClassifier     |  all        |  62.02       | 
| RandomForestClassifier     |  5000       |  76.63       | 
| RandomForestClassifier     |  10000      |  75.87       | 
| RandomForestClassifier     |  all        |  74.13       | 
| GradientBoostingClassifier |  5000       |  72.80       | 
| GradientBoostingClassifier |  10000      |  73.78       | 
| GradientBoostingClassifier |  all        |  72.53       | 
| VotingClassifier           |  5000       |  81.70       | 
| VotingClassifier           |  10000      |  80.94       | 
| VotingClassifier           |  all        |  81.66       | 
| MLP                        |  5000       |  80.01       | 
| MLP                        |  10000      |  79.65       | 
| MLP                        |  all        |  79.79       | 

