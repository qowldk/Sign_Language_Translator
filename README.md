![서비스 화면](https://github.com/qowldk/Sign_Language_Translator/blob/main/%EC%84%9C%EB%B9%84%EC%8A%A4%20%ED%99%94%EB%A9%B4.png)

-----
# Sign_Language_Translator
농인, 비농인 모두를 위한 실시간 수어 통역 서비스 입니다. 통역 과정을 실시간으로 제공하여 농인과 비농인 사이의 의사소통 격차를 해결하는 것이 저희 서비스의 핵심입니다. 



## 👨‍🏫 서비스 목적
청각, 언어 장애 인구는 계속해서 증가하는 추세인 반면 이들의 말을 전달해 주는 수어 통역사의 지원자 수는 매년 줄어들고 있습니다. 수어 통역이 필요한 상황에서 수어 번역기를 사용할 수 있게 된다면, 수어 통역사를 기다리지 않고 농인과 비농인간의 일상적인 의사소통이 가능할 것입니다.



## 📝 프로젝트 아키텍쳐 
![프로젝트 아키텍쳐](https://github.com/qowldk/Sign_Language_Translator/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EC%95%84%ED%82%A4%ED%85%8D%EC%B3%90.jpg)


## ⚙️ 기술 스택
저희 서비스는 React로 프론트엔드를 구성하였습니다. AI 서버는 Python과 OpenCV, MediaPipe 등 여러 라이브러리를 활용했습니다. 

유저가 서비스에 접속해 웹캠으로 비디오를 전송하면 WebSocket을 통해 서버와의 실시간 통신을 하게 되고, AI 서버에서 도출해낸 결과값을 유저에게 돌려주는 방식으로 통신하였습니다. 

## 시나리오
![시나리오](https://github.com/qowldk/Sign_Language_Translator/blob/main/%EA%B8%B0%EB%8A%A5.png)

1. 사용자가 웹캠 앞에서 수어 동작을 한다.
   - 이때 프레임별 각도 데이터가 쌓인다. 이를 학습된 모델과 비교하고, 인식된 단어들을 리스트에 저장한다.
2. 표현하고자 하는 수어 동작들을 수행한 후 문장 생성 버튼을 누르면 표현하고자 한 문장이 출력된다.
   - 인식된 단어들을 토대로 GPT Api를 거쳐 문장을 생성하여 websocket을 통해 화면에 출력한다.
3. 사용자는 수어가 문장으로 번역된 출력문을 확인 할 수 있다.


## 📌 주요 기능
### 지문자 인식

![지문자 인식](https://github.com/qowldk/Sign_Language_Translator/blob/main/%EC%A7%80%EB%AC%B8%EC%9E%90%20%EC%9D%B8%EC%8B%9D.png)


### 동적 수어 인식 

![동적 수어 인식](https://github.com/qowldk/Sign_Language_Translator/blob/main/%EB%8F%99%EC%A0%81%20%EC%88%98%EC%96%B4%20%EC%9D%B8%EC%8B%9D.png)


### ChatGPT API를 사용한 문장 생성 서비스

![ChatGPT API를 사용한 문장 생성 서비스](https://github.com/qowldk/Sign_Language_Translator/blob/main/gpt%20api.png)


## ⏲️ 개발 기간
2024.02.02 ~ 2024.06.26
