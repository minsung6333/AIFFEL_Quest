# AIFFEL Campus Online Code Peer Review Templete
<<<<<<< HEAD
- 코더 : 박태하
- 리뷰어 : 김지원


# PRT(Peer Review Template)
- [ ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인: 
        - **네, 확인하였습니다**
=======
- 코더 : 서민성
- 리뷰어 : 김태민

# PRT(Peer Review Template)
- [ ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
      - 잘 작성했습니다.
>>>>>>> b6facf8025312170db906fb26c1507208132c25e
    - 문제를 해결하는 완성된 코드란 프로젝트 루브릭 3개 중 2개, 
    퀘스트 문제 요구조건 등을 지칭
      - 잘 작성했습니다.
        - 해당 조건을 만족하는 코드를 캡쳐해 근거로 첨부
<<<<<<< HEAD
        - **Q1: Diabetes Multiple Linear Regression**
            - **Tasks들을 잘 follow-up 하야, 최종 performance 인 MSE Loss 3000 이하를 달성함**
            - **각 각 task에 만족하는 코드들을 근거로 첨부하겠음**
       - **Q2: Bike sharing Multiple Linear Regression**
           - **Tasks들을 잘 follow-up 하여 최종 결과인 RMSE 150 이하를 달성하였음**
           - **각 각 task에 만족하는 코드들을 근거로 첨부하겠음**
           - 예) 모델를 평가하기 위해서 dataframe을 만들었음. 주석은 비록 없었지만, 어떻게 만들었는지 잘 알겠음. 저도 이러한 부분 참고할 예정.
=======

1. 프로젝트 1의 회귀모델 예측정확도가 기준 이상 높게 나왔는가?

   ![image](https://github.com/minsung6333/AIFFEL_Quest/assets/29370771/c7401206-db52-4741-b4bb-230141c4df26)

2. 프로젝트 2의 회귀모델 예측정확도가 기준 이상 높게 나왔는가?

   ![image](https://github.com/minsung6333/AIFFEL_Quest/assets/29370771/017448ba-8906-45f8-85d3-e3564fc73785)

3. 시각화 요구사항이 정확하게 이루어졌는가?

   프로젝트 1번
   - ![image](https://github.com/minsung6333/AIFFEL_Quest/assets/29370771/f2ee7113-fb5a-4b2f-8017-9dac7209e480)

   프로젝트 2
   - ![image](https://github.com/minsung6333/AIFFEL_Quest/assets/29370771/dce91e5d-394a-4bc2-9511-d15a48993d30)
   - ![image](https://github.com/minsung6333/AIFFEL_Quest/assets/29370771/e3813506-4f9f-49fc-9735-b0e7f94a0749)
   - ![image](https://github.com/minsung6333/AIFFEL_Quest/assets/29370771/a4f836ac-9313-4a18-a7e2-e6fcc2b5730b)

>>>>>>> b6facf8025312170db906fb26c1507208132c25e
    
- [ ]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
<<<<<<< HEAD
        - **Q1: Diabetes Multiple Linear Regression**
            - **주석 또는 doc string을 잘 찾아보지 못했다.**
        - **Q2: Bike sharing Multiple Linear Regression**
            - **주석을 찾을 수 있었음. e.g. features selection 을 이렇게 한 이유. 하지만 통계적 방법 및 data visualization 방법들을 더 찾아보면 좋을것 같습니다. 
    - 해당 코드가 무슨 기능을 하는지, 왜 그렇게 짜여진건지, 작동 메커니즘이 뭔지 기술.
        - **Q1**
            - **중요한 포인트들이 기술되지 않은 느낌이 들었다.**
        - **Q2**
            - **코드에 대한 주석은 간결하게 있었음. 더 자세히 적어놓으면 좋을것 같음.**
    - 주석을 보고 코드 이해가 잘 되었는지 확인
        - 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부합니다.
        - **Q1**
            - 예
        - **Q2**
            - 예
=======
      - 잘 작성했습니다.
    - 해당 코드가 무슨 기능을 하는지, 왜 그렇게 짜여진건지, 작동 메커니즘이 뭔지 기술.
      - 기울기를 구하는 gradient 함수 구현하기
      - 주어진 입력 변수(X, W, b, y)에 대한 경사하강법을 수행하는 코드이다.
      - 가중치와 편향에 대한 편미분 값을 계산하여 모델의 파라미터를 업데이트 하는데 사용합니다.
    - 주석을 보고 코드 이해가 잘 되었는지 확인
        - 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부합니다.


    - ![image](https://github.com/minsung6333/AIFFEL_Quest/assets/29370771/4f019c85-268d-488a-9f0f-d28bb8df05af)

>>>>>>> b6facf8025312170db906fb26c1507208132c25e
        
- [ ]  **3. 에러가 난 부분을 디버깅하여 문제를 “해결한 기록을 남겼거나” 
”새로운 시도 또는 추가 실험을 수행”해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
<<<<<<< HEAD
        - **Q1: Diabetes Multiple Linear Regression**
            - 회고에서 그러한 부분을 찾을 수 있었다. trouble-shooting 한 흔적이 글로 적혀져있었다. 
    - 문제에서 요구하는 조건에 더해 추가적으로 수행한 나만의 시도, 실험이 기록되어 있는지 확인
        - **Q1:**
            - 회고에서 그러한 부분을 찾을 수 있었음
        - **Q2:**
            - 에러 혹은 트러블슈팅 부분을 찾을 수 없었음.
        - 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부합니다. 
=======
      - 문제의 원인과 해결 과정을 잘 작성했습니다.
    - 문제에서 요구하는 조건에 더해 추가적으로 수행한 나만의 시도, 
    실험이 기록되어 있는지 확인
      - 본인만의 좋은 하이퍼파라미터를 찾기위해 테스트를 진행했습니다.
        - 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부합니다.
        - ![image](https://github.com/minsung6333/AIFFEL_Quest/assets/29370771/b024586a-9f58-485f-8138-b9cb39576024)

>>>>>>> b6facf8025312170db906fb26c1507208132c25e
        
- [ ]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
      - 잘 작성되었습니다.
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인
<<<<<<< HEAD
        - **Q1:**
            - 네, 배운점 아쉬운 점 느낀점등이 보였고, 어떻게 하면 더 모델을 더 좋게 만들지도 나와있었다. 
        - 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부합니다. 
        - **Q2:**
            - 회고는 2문장 길이로 아주 간단하게 적혀져있었음. 변수 선정을 달리 해본것들에 대한 결과도 설명되어있으면 더 좋을거 같음.
=======
      - 없습니다. 
        - 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부합니다.
        - 프로젝트 1번에 대해서 잘 작성하셨고, 사이트 인용을 잘 하셨습니다.
        - ![image](https://github.com/minsung6333/AIFFEL_Quest/assets/29370771/5ffd0806-0c2d-4882-8aa7-bd37a46222df)

>>>>>>> b6facf8025312170db906fb26c1507208132c25e
        
- [ ]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
      - 잘 준수했습니다.
    - 하드코딩을 하지않고 함수화, 모듈화가 가능한 부분은 함수를 만들거나 클래스로 짰는지
      - model 함수, MSE 함수, loss 함수, gradient 함수를 잘 작성했습니다.
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화했는지
      - 잘 수행했습니다.
        - 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부합니다.
<<<<<<< HEAD
        - **Q1:**
            - Functions 중에 loss 와 관련있는 "MSE" function는 비록 capitalize가 되어있었지만, pronoun 으로 받아들여지는 것이 있어서 괜찮을것 같음
        - **Q2:**
            - 네, 그래프 만들때에 `for` 문을 적당히 사용했음
=======
        - ![image](https://github.com/minsung6333/AIFFEL_Quest/assets/29370771/7386a3e6-0d9b-4713-afaa-dc9d9c8c2dc7)

>>>>>>> b6facf8025312170db906fb26c1507208132c25e


# 참고 링크 및 코드 개선
```
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.
```
