# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 서민성
- 리뷰어 : 이명준


## 루브릭
1. 다양한 방법으로 Text Classification 태스크를 성공적으로 구현하였다.
> 3가지 이상의 모델이 성공적으로 시도되었다
    <img width="185" alt="image" src="https://github.com/Chancecatch1/AIFFEL_Quest_ms/assets/129345591/aeba622e-7942-470b-808d-b4aa5f81c88a">

    
2. gensim을 활용하여 자체학습된 혹은 사전학습된 임베딩 레이어를 분석하였다.
> gensim의 유사단어 찾기를 활용하여 자체학습한 임베딩과 사전학습 임베딩을 비교 분석함
    <img width="913" alt="image" src="https://github.com/Chancecatch1/AIFFEL_Quest_ms/assets/129345591/85874c2b-d021-47a0-bad0-5a3916630dd4">
    <img width="493" alt="image" src="https://github.com/Chancecatch1/AIFFEL_Quest_ms/assets/129345591/28bf68fc-a62c-48ab-b5a3-60e3d3447b13">
    

3. 한국어 Word2Vec을 활용하여 가시적인 성능향상을 달성했다.
> 네이버 영화리뷰 데이터 감성분석 정확도를 85% 이상 달성함
    <img width="750" alt="image" src="https://github.com/Chancecatch1/AIFFEL_Quest_ms/assets/129345591/81630539-a989-44c4-a0f3-f9aa6e686c94">


# PRT(Peer Review Template)
- [X]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 3가지 모델을 시도하였고, 한국어 W2V 임베딩을 활용하여 성능을 향상시키고 유사단어 찾기도 수행했다. 유사단어를 확인하는 과정을 통해서 모델별 어떤 차이가 있는지 리뷰어도 확인할 수 있었다.

    
- [X]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 아래 Fine Tuning 등 여러가지 중요 포인트에 주석이 잘 작성되었다. 
      <img width="837" alt="image" src="https://github.com/Chancecatch1/AIFFEL_Quest_ms/assets/129345591/8adba435-062f-41d0-a04b-880df765e36e">

        
- [X]  **3. 에러가 난 부분을 디버깅하여 문제를 “해결한 기록을 남겼거나” ”새로운 시도 또는 추가 실험을 수행”해봤나요?**
      - 소요되는 학습시간으로 인하여 실험을 도중에 중단하였지만, bert를 활용한 학습을 시도하였다.
      https://colab.research.google.com/drive/1tIf0Ugdqg4qT7gcxia3tL7und64Rv1dP#scrollTo=H5mANMwKkA0D

        
- [X]  **4. 회고를 잘 작성했나요?**
      <img width="866" alt="image" src="https://github.com/Chancecatch1/AIFFEL_Quest_ms/assets/129345591/78941720-ef7e-4488-83e1-d017d874f50f">

        
- [X]  **5. 코드가 간결하고 효율적인가요?**
    - 전체적으로 코드가 간결하고 효율적으로 작성되었다. 제한된 시간안에 최대한의 시도를 하고, 좋은 결과를 얻은 점에서 리뷰어 역시 많은 도움이 되었다.!


# 참고 링크 및 코드 개선
```
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.
```
