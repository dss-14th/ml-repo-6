Fast Campus DSS 14th ML Project-6조
# Machine Running Project - Machine Running을 활용한 소설 작가 분류

Machine Running Algorithm 모델을 활용하여 텍스트 데이터를 분석하여 test data를 분류 및 예측

- 주제 : 문체 분석 알고리즘 개발
- 배경 : 작가의 글을 분석하여 특징 도출
- 목적 : 작가 소설 속 문장 특징 도출 및 문장뭉치 분석을 통한 작가 예측

## Goals

DACON 소설 작가 분류 AI 경진대회 Data 사용
- Text Data EDA 진행(형태소 및 작가 별 특징 분석)

Text Data 분석을 위한 문장 벡터화
- Count Vectorizer : 단어들의 카운트(출현 빈도(frequency))로 여러 문서들을 벡터화
- Tfidf Vectorizer : TF-IDF vectorizer 는 문서를 tf-idf의 feature matrix로 변환하는 클래스

각 문장 간의 유사도 및 거리 측정
- Cosine 유사도 측정 : 두 개의 벡터값에서 코사인 각도를 구하는 방식(방향성이 함께 포함되어 괜찮은
성능을 가지는 것으로 알려짐
- 유클리드 유사도 측정 : 두 벡터사이의 거리를 구하는 방법 

다양한 머신러닝 분류 알고리즘 적용하여 문장 별 작가분류 성능 확인
- LogisticRegression, MultinomialNB, RandomForestClassifier,
DecisionTreeClassifier, AdaBoostClassifier, GradientBoostingClassifier,
LGBMClassifier, KNeighborsClassifier, LinearSVC, XgBoost, RidgeClassifier,
SGDClassifier 등 총 12개의 분류 알고리즘 적용
- 



## 팀구성

- 담당
김형기 :
여영웅 :


