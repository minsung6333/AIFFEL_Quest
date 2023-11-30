# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 서민성
- 리뷰어 : 김지원


# PRT(Peer Review Template)
- [ x ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
    - 문제를 해결하는 완성된 코드란 프로젝트 루브릭 3개 중 2개, 
    퀘스트 문제 요구조건 등을 지칭
        - 해당 조건을 만족하는 코드를 캡쳐해 근거로 첨부
- **Reviewer's comments**
    - 전처리, Mecab 기반 corpus 만들기가 잘되어있습니다 
    - 사전 훈련된 한국어 embedding 모델을 `ko.bin`으로 받고, substitution 하고자 하는 sentence에 대해서 lexical substitution 하는 function을 구현했습니다 
    - 데이터 토큰나이저를 구현하고 padding을 적용했습니다
    - 모델링을 했습니다 
        - Positional encoding 
        - Mask 생성
        - 네트워크 모델 
    - 훈련을 했습니다
    - Evaluation
        
```python
def lexical_sub(sentence, word2vec):

    res = []
    toks = sentence

    try:
        _from = random.choice(toks)
        _to = word2vec.most_similar(_from)[0][0]

    except:   # 단어장에 없는 단어
        return None

    for tok in toks:
        if tok is _from: res.append(_to)
        else: res.append(tok)

    return res
    ----
#이전 결과 기록용
arg_que_corpus = []
arg_ans_corpus = []

for j in range(3):
    if j==0:
        for i in tqdm(range(len(que_corpus))):
            que_temp = lexical_sub(que_corpus[i], wv)
            if que_temp == None: #단어장에 없어서 lexical_sub가 안되는 경우 제외 진행
                pass
            else:
                arg_que_corpus.append(que_temp)
                arg_ans_corpus.append(ans_corpus[i])
    elif j==1:
        for i in tqdm(range(len(que_corpus))):
            ans_temp = lexical_sub(ans_corpus[i], wv)
            if ans_temp == None: #단어장에 없어서 lexical_sub가 안되는 경우 제외 진행
                pass
            else:
                arg_que_corpus.append(que_corpus[i])
                arg_ans_corpus.append(ans_temp)
    elif j==2:
        for i in tqdm(range(len(que_corpus))):
            arg_que_corpus.append(que_corpus[i])
            arg_ans_corpus.append(ans_corpus[i])
```
    
- [ ]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드가 무슨 기능을 하는지, 왜 그렇게 짜여진건지, 작동 메커니즘이 뭔지 기술.
    - 주석을 보고 코드 이해가 잘 되었는지 확인
        - 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부합니다.
- **Reviewer's comments**
    - 주석이 있는곳도 있고, 없는곳도 있다 
    - annotation/doc string은 보기 어려웠다
        
- [ ]  **3. 에러가 난 부분을 디버깅하여 문제를 “해결한 기록을 남겼거나” 
”새로운 시도 또는 추가 실험을 수행”해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
    - 문제에서 요구하는 조건에 더해 추가적으로 수행한 나만의 시도, 
    실험이 기록되어 있는지 확인
        - 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부합니다.
- **Reviewer's comments**
    - NLTK를 이용한 BLEU Score를 확인을 많이 수행했다 
```python

eval_bleu_single(transformer, 
                 '지루하다, 놀러가고 싶어.', 
                 '잠깐 쉬 어도 돼요 .', 
                 tokenizer,
                 tokenizer,
                 mecab)
```
        
- [ ]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인
        - 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부합니다.
- **Reviewer's comments**
    - 회고가 따로 없었지만, 문제가 발생한 곳에 대해서 다른 그루의 도움을 요청하였다.
    
- [ ]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
    - 하드코딩을 하지않고 함수화, 모듈화가 가능한 부분은 함수를 만들거나 클래스로 짰는지
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화했는지
        - 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부합니다.
- **Reviewer's comments**
    - 네, 간결한것 같습니다


# 참고 링크 및 코드 개선
```
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.
```
