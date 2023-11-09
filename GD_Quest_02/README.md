# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 서민성
- 리뷰어 : 김서연


# PRT(Peer Review Template)
- [ ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - <img width="680" alt="스크린샷 2023-11-09 오후 5 43 15" src="https://github.com/minsung6333/AIFFEL_Quest/assets/112914475/fb62f91c-6536-44dd-8e41-f0b2763816b4">
    - 단어 개수 별로 각 모델의 정확도를 시각화를 통해 비교하였다.
    - F1-score의 비교, 딥러닝 모델과의 비교가 아직 이뤄지지 않았다.
    
- [ ]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - ```python3
      # 데이터 호출 및 가공
        from sklearn.feature_extraction.text import CountVectorizer
        from sklearn.feature_extraction.text import TfidfTransformer
        from tensorflow.keras.datasets import reuters
        word_index = reuters.get_word_index(path="reuters_word_index.json")
        
        # 인덱스 수정을 위한 전처리
        index_to_word = { index+3 : word for word, index in word_index.items() }
        dtmvector = CountVectorizer()
        tfidf_transformer = TfidfTransformer()
        
        
        # index_to_word에 숫자 0은 , 숫자 1은 , 숫자 2는 를 넣어줍니다.
        for index, token in enumerate(("", "", "")):
          index_to_word[index]=token
        print('=3')
        
        # 데이터 전처리를 위한 가공함수 생성
        def data_tfidf(num_words):
          (x_train, y_train), (x_test, y_test) = reuters.load_data(num_words= num_words, test_split=0.2)
        
          # #decoding
          decode_train = []
          decode_test = []
        
          for i in range(len(x_train)):
            t = ' '.join([index_to_word[index] for index in x_train[i]])
            decode_train.append(t)
        
          for i in range(len(x_test)):
            q = ' '.join([index_to_word[index] for index in x_test[i]])
            decode_test.append(q)
        
          x_train = decode_train
          x_test = decode_test
        
        
          x_train_dtm = dtmvector.fit_transform(x_train) #dtm 행렬 생성
          tfidfv = tfidf_transformer.fit_transform(x_train_dtm) #tf-idf 행렬 생성
        
          x_test_dtm = dtmvector.transform(x_test) #테스트 데이터를 DTM으로 변환
          tfidfv_test = tfidf_transformer.transform(x_test_dtm) #DTM을 TF-IDF 행렬로 변환
        
          return x_train, y_train, x_test, y_test, tfidfv, tfidfv_test
      ```
  - 전처리 과정을 주석으로 잘 설명했다. 함수 내부에도 주석이 추가되면 좋을 것 같다.
        
- [ ]  **3. 에러가 난 부분을 디버깅하여 문제를 “해결한 기록을 남겼거나” 
”새로운 시도 또는 추가 실험을 수행”해봤나요?**
    - 데이터 전처리 과정에서 데이터가 원하는대로 잘 변환되고 있는지 확인하는 과정이 있으면 좋을 것 같다.
    - 가능한 추가 실험으로 딥러닝 모델도 2개 이상을 시도해보는 것 등이 있을 것이다.
        
- [ ]  **4. 회고를 잘 작성했나요?**
    - 회고가 아직 작성되지 않았다.
        
- [ ]  **5. 코드가 간결하고 효율적인가요?**
    - 위 코드 블럭에서처럼 전처리 과정의 일부를 함수화하였다.
    - ```python3
     for i in ml_lst:
  print(str(i))
  tqdm(i.fit(tfidfv, y_train))
  predicted = i.predict(tfidfv_test) #테스트 데이터에 대한 예측
  # print("정확도:", accuracy_score(y_test, predicted)) #예측값과 실제값 비교
  df = pd.DataFrame(classification_report(y_test, i.predict(tfidfv_test), zero_division=0, output_dict=True)).transpose()
  precision_25000.append(df['precision'].values.tolist())
  recall_25000.append(df['recall'].values.tolist())
  f1_score_25000.append(df['f1-score'].values.tolist())
   ```
    모델 학습 및 예측 부분에서 위 코드가 반복되는데 이 부분을 함수화하면 코드의 가독성이 올라갈 것이다.

# 참고 링크 및 코드 개선
```
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.
```
