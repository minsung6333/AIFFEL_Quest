# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 서민성
- 리뷰어 : 김서연


# PRT(Peer Review Template)
- [ ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - <img width="937" alt="스크린샷 2023-12-04 오후 5 23 40" src="https://github.com/minsung6333/AIFFEL_Quest/assets/112914475/2d1c7411-362a-45c0-b864-fa5c533c6c40">
    - 데이터셋이 잘 생성되었다.
    - <img width="919" alt="스크린샷 2023-12-04 오후 5 24 33" src="https://github.com/minsung6333/AIFFEL_Quest/assets/112914475/6c061995-8d5a-4187-b67d-4bdcb18a6327">
    - 학습이 안정적으로 진행되는 과정을 시각화하였다.
    
- [ ]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    ```python3
    def lm_acc(y_true, y_pred):
        """
        acc 계산 함수
        :param y_true: 정답 (bs, n_seq)
        :param y_pred: 예측 값 (bs, n_seq, n_vocab)
        """
        # 정답 여부 확인
        y_pred_class = tf.cast(K.argmax(y_pred, axis=-1), tf.float32)
        matches = tf.cast(K.equal(y_true, y_pred_class), tf.float32)
        # pad(0) 인 부분 mask
        mask = tf.cast(tf.math.not_equal(y_true, 0), dtype=matches.dtype)
        matches *= mask
        # 정확도 계산
        accuracy = K.sum(matches) / K.maximum(K.sum(mask), 1)
        return accuracy
    ```
    - 주석이 잘 작성되어있다.
               
- [ ]  **3. 에러가 난 부분을 디버깅하여 문제를 “해결한 기록을 남겼거나” 
”새로운 시도 또는 추가 실험을 수행”해봤나요?**
    - <img width="989" alt="스크린샷 2023-12-04 오후 5 29 55" src="https://github.com/minsung6333/AIFFEL_Quest/assets/112914475/a81cffcf-8d43-4f70-a783-4dcec49d57d4">
    - 데이터 크기와 epoch을 조정하여 실험 수행
        
- [ ]  **4. 회고를 잘 작성했나요?**
    - 회고가 작성되지 않았다.
      
- [ ]  **5. 코드가 간결하고 효율적인가요?**
    - 주요 함수들을 모듈화하여 잘 작성하였다.

# 참고 링크 및 코드 개선
```
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.
```
