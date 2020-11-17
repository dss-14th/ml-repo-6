Fast Campus DSS 14th ML Project-6조
# Machine Learning을 활용한 소설 작가 분류모델

Machine Learning Algorithm 모델을 활용하여 작가 텍스트 데이터를 분석하여 test data의 작가 분류 및 예측

- 주제 : 문체 분석 알고리즘 개발
- 배경 : 작가의 글을 분석하여 특징 도출
- 목적 : 작가 소설 속 문장 특징 도출 및 문장뭉치 분석을 통한 작가 예측
- DATA 출처 : ACON 소설 작가 분류 AI 경진대회 Data 사용


## Process
-----------------------------------------------------

> 1. Text Data EDA 진행(형태소 및 작가 별 특징 분석)

<img src="https://user-images.githubusercontent.com/65877745/99362453-dd9c3580-28f6-11eb-942b-f66e2da11fc9.png" width="60%" height="60%" alt="process"></img>
<img src="https://user-images.githubusercontent.com/65877745/99362501-eee54200-28f6-11eb-8f94-d4fbabfaa5b0.png" width="60%" height="60%" alt="process"></img>


> 2. 각 문장 간의 유사도 및 거리 측정
>   >- 유클라디안 거리 측정 : 두 벡터 사이의 거리를 구하는 방법
<img src="https://user-images.githubusercontent.com/65877745/99362230-90b85f00-28f6-11eb-8f70-95cfe4f463e0.png" width="60%" height="60%" alt="process"></img>
>   >- Cosine 유사도 측정 : 두 개의 벡터값에서 코사인 각도를 구하는 방식(방향성이 함께 포함되어 괜찮은 성능으로 알려짐)
<img src="https://user-images.githubusercontent.com/65877745/99361918-27d0e700-28f6-11eb-95fd-916f8d5b5a5e.png" width="60%" height="60%" alt="process"></img>
>   >- 각 유사도를 구하고 가장 유사하거나 거리가 가까운 문장을 찾아서 비교

MultinomialNB 알고리즘을 base line 으로 잡고 다양한 분류 알고리즘을 적용

>3. LogisticRegression, MultinomialNB, RandomForestClassifier, DecisionTreeClassifier, AdaBoostClassifier, GradientBoostingClassifier,
LGBMClassifier, KNeighborsClassifier, LinearSVC, XgBoost, RidgeClassifier,
SGDClassifier 등 총 12개의 분류 알고리즘 적용 후 5개 가장 성능(Accuracy)이 높게 나온 5개 분류 모델 선정(LinearSVC, SGD Classifier, LogisticRegression, RidgeClassifier, Multinomial NB)

>4. 선정된 분류모델에 TF-IDF-parameter Tuning을 통해 parameter 값 설정
<img src="https://user-images.githubusercontent.com/65877745/99363429-138de980-28f8-11eb-986e-753e6ed177e8.png" width="60%" height="60%" alt="process"></img>

>5. NLTK의 Stopwords에 예측이 틀린 Text Data 중 가장 빈도수가 높은 단어 추가하여 진행하였으나, Test ACC 3% 가량 하락

>6. LDA : 토픽 모델링 시각화
<img src="https://user-images.githubusercontent.com/65877745/99363235-d7f31f80-28f7-11eb-9627-a2b30a115bbe.png" width="60%" height="60%" alt="process"></img>


## 팀구성

* 김형기 : TfidfVectorizer, 모델링, 토픽 모델링(LDA)
* 여영웅 : 코사인 유사도, 유클리디안 유사도 및 머신러닝 학습


