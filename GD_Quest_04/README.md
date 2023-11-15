# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 서민성
- 리뷰어 : 김서연


# PRT(Peer Review Template)
- [ ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    ```python3
    def preprocess_sentence(sentence, s_token=False, e_token=False):
        sentence = sentence.lower().strip()
    
        sentence = re.sub(r"([?.!,])", r" \1 ", sentence)
        sentence = re.sub(r'[" "]+', " ", sentence)
        sentence = re.sub(r"[^a-zA-Z?.!,ㄱ-ㅎ가-힣0-9]+", " ", sentence)
    
        sentence = sentence.strip()
    
        if s_token:
            sentence = '<start> ' + sentence
    
        if e_token:
            sentence += ' <end>'
        
        return sentence
    ```
    - 한국어를 포함해 텍스트 데이터 전처리가 잘 이루어졌다.
  <img width="695" alt="스크린샷 2023-11-15 오후 5 19 19" src="https://github.com/minsung6333/AIFFEL_Quest/assets/112914475/404aebd8-0330-4ceb-bf96-4f4f881f0003">
    - 훈련 과정에서 loss 값이 꾸준히 감소하였다.
     <img width="660" alt="스크린샷 2023-11-15 오후 5 20 30" src="https://github.com/minsung6333/AIFFEL_Quest/assets/112914475/128613e3-99af-4cd2-8858-6cbd8012b1d0">
    <img width="644" alt="스크린샷 2023-11-15 오후 5 20 56" src="https://github.com/minsung6333/AIFFEL_Quest/assets/112914475/af8ef0a7-de3c-486e-9c4a-39b75b110719">
    <img width="638" alt="스크린샷 2023-11-15 오후 5 21 15" src="https://github.com/minsung6333/AIFFEL_Quest/assets/112914475/4fa4099b-b038-4119-a0ca-18e25c58f8a9">
  - 한국어 문장을 입력하면 영어 문장이 나오기는 하지만 의미있는 번역이라고 보긴 어렵다. (+ 그러나 일단 문장이 나온다는 것만으로도 큰 성과라 생각합니다...)


- [ ]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
   ```python3
    data_path = os.getenv('HOME')+'/aiffel/korean_english_aihub' #파일경로설정
    
    with open(data_path+'/일상생활및구어체_한영_train_set.json') as f: 
        js = json.loads(f.read()) ## json 라이브러리 이용
    
        
    num_data = 30000
        
    df = pd.DataFrame(js['data']) #데이터 프레임 생성
    data = df[['ko','en']].iloc[:num_data] #데이터 추출
    
    enc_corpus = []
    dec_corpus = []
    
    for i in tqdm(range(len(data))):
        enc_corpus.append((preprocess_sentence(data['ko'][i])))
        dec_corpus.append(preprocess_sentence(data['en'][i], s_token=True, e_token=True))
        
    print("kor:", enc_corpus[100])   # go away !
    print("eng:", dec_corpus[100])   # <start> salga de aqu ! <end>
   ```
   - 전처리 과정에서 주석으로 설명이 잘 되어있다.
   - 학습 모델과 학습 과정 코드에도 주석이 있다면 좋을 것 같다.
     
- [ ]  **3. 에러가 난 부분을 디버깅하여 문제를 “해결한 기록을 남겼거나” 
”새로운 시도 또는 추가 실험을 수행”해봤나요?**
    - 공백 기반 토큰화, 형태소 기반 토큰화를 각각 시도했다.
        
- [ ]  **4. 회고를 잘 작성했나요?**
    - <img width="888" alt="스크린샷 2023-11-15 오후 5 27 28" src="https://github.com/minsung6333/AIFFEL_Quest/assets/112914475/5e9c8eb1-59d1-4ff2-a4b5-aa99585b72bd">
    - 회고가 잘 작성되었다.

        
- [ ]  **5. 코드가 간결하고 효율적인가요?**
```python3
# kor_tokenizer = tokenize(kor_corpus)[1]
dec_tokenizer = tokenize(dec_corpus)[1]

# kor_tensor = tokenize(kor_corpus)[0]
dec_tensor = tokenize(dec_corpus)[0]

enc_train, enc_val, dec_train, dec_val = \
train_test_split(enc_tensor, dec_tensor, test_size=0.2)
```
- 주석 처리한 코드에 대해 이유가 나와있으면 더 좋을 것 같다.


# 참고 링크 및 코드 개선
```
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.
```
