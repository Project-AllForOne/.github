# ✨ 프로젝트 : 방향(訪香) - AI 기반 향수 추천 웹서비스
![image](https://github.com/user-attachments/assets/a9833edf-ad21-4ebd-b65d-0e273dfa7e5a)

## 📅 프로젝트 기간
2024.10.28 ~ 2024.12.16 (총 36일)

## 💡 방향(訪香)이란?
향기는 뇌의 편도체와 해마에 직접적으로 작용하여 다른 어떤 감각보다 빠르게 뇌에 전달됩니다.   
그래서 향기는 기억이나 추억을 떠올릴 때에 가장 강력히 작용합니다.   
이토록 우리가 모르는 사이 순식간에 우리를 스치는 향기는   
더이상 감추기 위한 도구가 아니라 나를 표현하는 고유한 향기가 되었습니다.

## ✔ 방향(訪香)이 제시하는 방향(方向)
코로나 19 이후로 실내에 머무는 시간이 증가하며 관심과 수요가 꾸준히 증가하고,   
2025년엔 무려 1조원 규모의 시장 형성이 예상되는 향수.   
***여러분은 어떻게 사용하고 계신가요?***

향수를 구매하려면 보통 오프라인 매장에 방문하여 시향하는 것이 일반적입니다.   
하지만 수많은 브랜드와 수많은 제품들을 모두 직접 방문하여 시향하기는 어렵습니다.   
반면 온라인에는 다양한 정보들이 있지만 시향이 불가능하고 모든 정보를 파악하기 어렵습니다.   
이러한 향수의 특징 때문에 향수를 소비하는 국내 소비자의 70%는,   
시향 경험 부족으로 구매 실패를 경험한 적이 있다고 합니다.   

방향(訪香)에선 이러한 소비자의 고민을 해결하기 위해 'AI 센티크'와의 대화로   
사용자가 원하는 향의 느낌을 들어보고 그에 맞는 향수를 제시해드립니다.   
***향수에 대한 정확한 설명이 아니어도 괜찮습니다.***   
당장 떠오르는 느낌이나 분위기나 상황, 또는 사진을 보여주시면 그에 어울리는 향수를 추천해드립니다.

## 🛠 방향(訪香)의 주요 기능
* 카카오 연동 회원가입
  + 카카오와 연동하여 카카오 계정 정보 그대로 회원가입과 로그인이 가능합니다.
  + 회원 탈퇴를 진행할 수 있습니다.
* 향료 알아가기
  + 방향(訪香)에 등록 되어있는 향료들의 정보를 조회할 수 있습니다.
  + 계열을 선택하여 해당 계열의 향료만 조회할 수 있습니다.
  + 향료의 이름을 검색하여 조회할 수 있습니다.
* 향수 알아가기
  + 방향(訪香)에 등록 되어있는 향수들의 정보를 조회할 수 있습니다.
  + 부향률을 선택하여 해당하는 향수만 조회할 수 있습니다.
  + 향수의 이름을 검색하여 조회할 수 있습니다.
* 향수 추천받기
  + AI 센티크와의 채팅으로 향수 추천이 이루어집니다.
  + 이전에 나눴던 채팅 기록을 조회할 수 있습니다.
  + 사용자는 텍스트 또는 이미지 또는 둘 다 사용하여 원하는 향수에 대한 느낌을 입력합니다.
  + 이미지 파일은 **salesforce**의 image to text model인 **BLIP**을 통해 내용을 분석합니다.
  + 사용자의 텍스트 입력값과 첨부 이미지 분석 결과를 **chatGPT**로 전송하여 향수 추천 결과와 이미지 생성 프롬프트를 생성합니다.
  + **chatGPT**를 통해 생성된 이미지 생성 프롬프트를 text to image model인 **Stable Diffusion**에 전송하여 피드백 이미지를 생성합니다.
  + 생성된 향수 추천 결과와 피드백 이미지를 사용자에게 제공합니다.
  + 추천 결과의 계열 정보에 따라 채팅창 UI의 색상이 함께 변화합니다.
  + 키워드를 검색하여 키워드가 포함된 채팅 결과를 조회할 수 있습니다.
  + 생성된 향수 추천 결과를 히스토리로 저장할 수 있습니다.
* 히스토리 조회
  + 저장했던 히스토리를 조회할 수 있습니다.
  + 저장된 히스토리를 이미지 파일로 제공받을 수 있습니다.
 
## 🥽 방향(訪香)이 사용한 기술
* Spring
  + IntelliJ IDEA
  + Spring Boot 3.3.5
  + Spring Cache
  + Spring Web
  + Spring Webflux
  + Spring Lombok
  + Spring JPA
  + MySQL
  + MongoDB
  + AWS S3
  + Postman
* Python
  + Visual Studio Code IDE
  + Fast API
  + uvicorn
  + ipywidgets
  + Accelerate
  + Selenium
  + Web driver manager
  + Base4 BeautifulSoup
  + MySQL connector
  + Langchain OpenAI
  + dotenv
  + Pillow
  + scikit learn
  + Transformers
  + Pytorch
  + diffusers
  + replicate
  + requests
* React
  + Visual Studio Code IDE
  + Redux
  + React Router DOM
  + Axios
* 협업 도구
  + GitHub
  + Notion
  + Discord
 
## 🗂 패키지 구조
* Spring
```
com
    └─banghyang
        ├─auth
        │  └─kakao
        │      ├─client
        │      ├─config
        │      ├─controller
        │      ├─model
        │      │  └─dto
        │      └─service
        ├─chat
        │  ├─controller
        │  ├─dto
        │  ├─entity
        │  ├─repository
        │  └─service
        ├─common
        │  ├─config
        │  ├─mapper
        │  ├─type
        │  └─util
        ├─history
        │  ├─controller
        │  ├─dto
        │  ├─entity
        │  ├─repository
        │  └─service
        ├─member
        │  ├─controller
        │  ├─dto
        │  ├─entity
        │  ├─repository
        │  └─service
        └─object
            ├─line
            │  ├─entity
            │  └─repository
            ├─note
            │  ├─entity
            │  └─repository
            ├─perfume
            │  ├─controller
            │  ├─dto
            │  ├─entity
            │  ├─repository
            │  └─service
            └─spice
                ├─controller
                ├─dto
                ├─entity
                ├─repository
                └─service
```
* Python
```
  .env
│  .gitignore
│  cache_timestamp.txt
│  main.py
│  perfume_cache.json
│
├─models
│  │  img_llm_client.py
│  │  line.json
│  │  prompt_template.json
│  └─ prompt_template.txt
│
├─routers
│  │  image_generation_description_router.py
│  │  image_generation_router.py
│  │  image_processing_router.py
│  └─ llm_router.py
│
├─services
│  │  db_service.py
│  │  image_generation_service.py
│  │  image_processing_service.py
│  │  llm_img_service.py
│  │  llm_service.py
│  └─ prompt_loader.py
│
└─utils
   └─ line_mapping.py
```
* React
```
├─api
├─components
│  ├─footer
│  ├─loading
│  ├─login
│  └─sidebar
├─css
│  ├─admin
│  ├─components
│  └─footer
├─layouts
├─module
└─pages
    ├─admin
    ├─booklist
    ├─chat
    ├─footer
    ├─history
    └─test
```
## 🏗 방향(訪香) 산출물
![image](https://github.com/user-attachments/assets/64d9b25c-59e5-499b-8a47-876fc4d18263)


## 🤲 방향(訪香) 팀원 소개
![image](https://github.com/user-attachments/assets/11b6ead7-ca84-43a9-9fdd-2ab691831ffb)

## 📐 방향(訪香)이 개선할 방향(方向)
* 전체적인 코드 컴포넌트 분리
* 향수 추천 답변 속도 개선
* 향수, 향료에 대한 양질의 데이터 확보
* 향수 추천 기준에 대한 전문가의 의견 반영
* 이미지 생성, 향수 추천 결과 프롬프트 개선
* 사용자가 서비스를 이용하며 향수에 대해 더 알 수 있고 관심이 가도록 정보 제공

## 🎞 프로젝트 진행 소감
* 성민 : 저는 이번 프로젝트에서 데이터 설계, 스프링 서버에서의 미들웨어 개발을 맡았습니다.   
처음으로 스프링에서 프론트와 API, 2종류의 서버와 통신해보았는데,   
개발할 당시엔 놓치고 있었지만 아키텍쳐의 윤곽이 어느정도 갖춰진 지금 살펴보면   
개선할 수 있는 부분이 많다는걸 깨달았습니다.   
우선 컴포넌트의 분리입니다.   
매퍼 메소드의 분리, 한 메소드에선 하나의 처리만 이루어지게 하는 설계,   
한 객체의 서비스 클래스에서 여러 객체의 레파지토리를 사용하는 등의 처리가 미흡했던 것 같습니다.   
그리고 동기, 비동기 처리의 선택입니다.   
사용자에게 입력을 받은 후에 향수 추천을 위한 모델 호출과 이미지 프롬프트 생성을 위한 모델 호출은 동시에 처리될 수 있는데   
동기적으로 처리하여 결과 도출까지의 시간 절약을 고려하지 못한 부분이 아쉽습니다.
마지막으로 자체적인 보안 시스템의 부재입니다.   
카카오 API와의 연동으로 카카오 계정의 정보를 가져와서 멤버 객체로 저장하고   
프론트에선 로컬 스토리지에 회원정보를 저장하여 회원, 비회원, 관리자에 대한 검증을 처리하는데,   
추후엔 세션 로그인이나 JWT를 이용하여 꼭 안전하게 처리하도록 하고싶습니다.   
프로젝트의 주제를 정하면서 향수라는 분야에 대해 잘 모르기 때문에 걱정을 많이 했었는데,   
개발후에 직접 기능을 사용해보면서 이 서비스가 만약 존재한다면   
실제로 쓰고 싶다는 생각이 들 정도로 괜찮다는 생각이 들었습니다.   
팀원들이 좋은 아이디어를 많이 내어주고 각자의 분야에서 열심히 개발해주어서   
걱정한것보다 더 좋은 결과를 만들어낸 것 같아서 뿌듯합니다.   
좋은 결과가 나온만큼 위의 개선점과 더불어 앞으로 방향 프로젝트를 더 개선해나가서   
실제로 상용화 될 수 있는 서비스로 거듭날 수 있도록 하고 싶습니다.
* 혜연 : 
* 강현 : 
* 성은 : 
* 규섭 : 저는 이번 프로젝트에서 향료백과 연동, 사이드바와 푸터 UI와 그 연동, 회원탈퇴를 맡았습니다. 이 프로젝트를 진행하며 여러 개선된 점과 다음 프로젝트에서 개선할 수 있는 점을 느꼈는데, 우선 프로젝트를 하며 느낀 개선될 수 있는 점부터 적어보겠습니다. 이슈트래킹은 이슈트래킹의 개념이 아직 안 잡혀 있었던 지난번보단 좀 더 많이 써놨지만 이슈 해결과 코딩에 급하다 보니 더 많은 이슈가 있었는데도 이슈트래킹에 잘 작성하지 못한 점이 아쉬웠습니다. 또한, 예상했던 시간보다 좀 더 오래 걸렸는데, 분담된 작업이 끝나고 시간이 남았을 때 다른 팀원들의 일을 좀 더 자발적으로 분담해서 같이 했으면 더 빨리 끝났을지도 모르겠다는 아쉬움이 있습니다. 개인적으로는, LLM을 다루는 것이 처음이다 보니 나름대로 노력했음에도 전체 구조 파악, 특히 AI 관련해서 아직 부족한 점이 많다고 느꼈습니다. 향료 백과의 백엔드-프론트엔드 연결의 경우 제가 전부 맡기로 했었는데 연결이 지난번보다 훨씬 익숙했는데도 온전하게 완성을 못하고 결국 팀원분들과 함께 완성하게 된 점이 아쉽게 느껴졌습니다. 마지막으로는, 강사님께서도 지적해주신 점이지만 향수 초보들에게 향수를 소개하겠다는 목적과 달리 향수 초보들이 잘 알 수 없는 부향률과 계열에 대한 설명을 좀 더 해볼 걸 그랬다고 느꼈습니다.

다음으로, 이 프로젝트를 통해 개선된 점을 적어보겠습니다. 우선, 지난 프로젝트에서 크게 부족하다고 느꼈던 프론트엔드와 백엔드의 구조 관련 이해가 개선됨에 따라 Front와 Back 연결을 좀 더 매끄럽게 할 수 있게 되었습니다. 다음으로는 Front 디자인에 너무 시간을 들여 연결할 시간이 부족했던 지난 프로젝트의 교훈을 살려 대략적인 모양만 비슷하게 만들고 backend와의 연결에 좀 더 노력을 기울인 결과 개인 작업에서 시간이 부족해 일을 끝내지 못하는 일은 없었으며, 그 외에도 컴파일 등 오류 발생시 해결능력이 늘었다고 느꼈습니다.
* 은혜 : 
