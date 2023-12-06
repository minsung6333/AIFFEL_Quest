# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 서민성
- 리뷰어 : 김지원

----
루브릭

1. 모델과 데이터를 정상적으로 불러오고, 작동하는 것을 확인하였다. 
    - klue/bert-base를 NSMC 데이터셋으로 fine-tuning 하여, 모델이 정상적으로 작동하는 것을 확인하였다.
2. Preprocessing을 개선하고, fine-tuning을 통해 모델의 성능을 개선시켰다.
- Validation accuracy를 90% 이상으로 개선하였다.
3. 모델 학습에 Bucketing을 성공적으로 적용하고, 그 결과를 비교분석하였다.
Bucketing task을 수행하여 fine-tuning 시 연산 속도와 모델 성능 간의 trade-off 관계가 발생하는지 여부를 확인하고, 분석한 결과를 제시하였다. 

---

# PRT(Peer Review Template)
- [ ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 모델과 데이터를 불러오고 작동하는지 확인했다. 또한 전처리를 모델에 넣을 수 있도록 만들었다.
        - klue/bert-base tokenizer와 모델을 블러와, 모델 인풋에 맞도록 잘 변경/전처리를 하였다 
   - Fine-tuning (Step 4) 그리고 Step 5는 하지 못하였다.
    
- [ ]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 데이터셋을 이렇게 저렇게 변경을 해보며, 확인을 해보았다. 
    
```python
# DataFrame 데이터를 dict 내부에 list로 변경
train_dataset = train_dataset.to_dict(orient='list')
val_dataset = val_dataset.to_dict('list')
test_dataset = test_dataset.to_dict('list')

# Hugging Face dataset으로 변환
tf_train_dataset = Dataset.from_dict(train_dataset)
tf_val_dataset = Dataset.from_dict(val_dataset)
tf_test_dataset = Dataset.from_dict(test_dataset)

```
        
- [ ]  **3. 에러가 난 부분을 디버깅하여 문제를 “해결한 기록을 남겼거나” 
”새로운 시도 또는 추가 실험을 수행”해봤나요?**
    - 코멘트가 남겨져있었다. 이렇게 데이터에 대한 확인을 한 기록을 남겼다
```
train/test 동일한 형식으로 되어있음
train 150k test 50k로 되어있음
```
        
- [ ]  **4. 회고를 잘 작성했나요?**
    - 화고는 없는것 같습니다
        
- [ ]  **5. 코드가 간결하고 효율적인가요?**
    - 네, 간결합니다. 
    - 저도 궁금한 점인데, pre-trained 을 이용하는 방법들도 몇 있던데, 이거는
    어떠한 방법인지 궁금하군요. 저도 한 번 찾아보겠습니다. 
        - 이러한 의문이 든 이유가 이렇게 이름을 지었는데, 궁금하네요.
        
```python
model_checkpoint = "klue/bert-base"
num_labels = 2
```


# 참고 링크 및 코드 개선
```
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.
```
