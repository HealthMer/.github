# ⏳ HealthMer

## 목차
1. [소개](#1소개)
2. [팀원](#2팀원)
3. [타임라인](#3타임라인)
4. [ERD](#4ERD)
5. [다이어그램](#5다이어그램)
6. [실행 화면](#6실행화면)
7. [트러블 슈팅](#7트러블-슈팅)
8. [핵심 경험](#8프로젝트-수행-중-핵심-경험)

## 1.소개
- 집에서 운동하는 홈트인들을 위한 서비스
- 직접 루틴 타이머 만들기
- 만든 루틴 타이머를 타인과 공유
<br>

## 2.팀원
| 백지민 | 윤병희 |
| :---: | :---: |
| <img src="https://avatars.githubusercontent.com/u/175587334?v=4" width="155" height="150">| <img src=https://i.imgur.com/jrW5RQj.png width="155" height="150" > |
|  [@지민_GitHub](https://github.com/eosa1414) | [@병희_GitHub](https://github.com/dylan-yoon) |

<br>

## 3.타임라인
<img width="1024" alt="스크린샷 2024-11-27 02 58 40" src="https://github.com/user-attachments/assets/d73fa9e4-5af5-438d-921c-6caa4afd6d9b">




<br>

## 4.ERD
![HealthMerERD-2](https://github.com/user-attachments/assets/831510f4-3fe9-47f9-a412-b4b0a58c2457)



## 5.다이어그램
#### 파일 구조
##### Front-Vue
```bash
├── src
│   ├── App.vue
│   ├── api
│   │   └── axiosInstance.js
│   ├── assets
│   │   ├── 7033786-uhd_3840_2160_25fps.mp4
│   │   ├── base.css
│   │   ├── logo-simple.svg
│   │   ├── main.css
│   │   ├── pexels-eye4dtail-114738.jpg
│   │   └── styles
│   │       ├── _global.css
│   │       ├── _reset.css
│   │       └── _variables.css
│   ├── components
│   │   ├── Btn.vue
│   │   ├── BtnToggle.vue
│   │   ├── Category.vue
│   │   ├── Footer.vue
│   │   ├── Header.vue
│   │   ├── InputField.vue
│   │   ├── Loading.vue
│   │   ├── Modal.vue
│   │   ├── SignForm.vue
│   │   ├── common
│   │   │   ├── Logo.vue
│   │   │   ├── LogoBasicSvg.vue
│   │   │   ├── LogoFullSvg.vue
│   │   │   └── LogoSimpleSvg.vue
│   │   ├── community
│   │   │   └── CommunityList.vue
│   │   ├── icons
│   │   │   ├── AddTimerSvg.vue
│   │   │   ├── MenuIconSvg.vue
│   │   │   └── PlayBtnIcon.vue
│   │   └── timer
│   │       ├── TimerCreate.vue
│   │       ├── TimerList.vue
│   │       └── TimerListItem.vue
│   ├── layouts
│   │   ├── DefaultLayout.vue
│   │   └── MinimalLayout.vue
│   ├── main.js
│   ├── router
│   │   └── index.js
│   ├── stores
│   │   ├── counter.js
│   │   ├── history.js
│   │   ├── theme.js
│   │   ├── timer.js
│   │   └── user.js
│   └── views
│       ├── CommunityListView.vue
│       ├── MainView.vue
│       ├── SigninView.vue
│       ├── SignupView.vue
│       ├── TimerDetailView.vue
│       └── TimerListView.vue
└── vite.config.js
```

##### Back-Spring
```bash
├── HealthMer
│   ├── HELP.md
│   ├── mvnw
│   ├── mvnw.cmd
│   ├── pom.xml
│   ├── src
│   │   ├── main
│   │   │   ├── java
│   │   │   │   └── com
│   │   │   │       └── minijean
│   │   │   │           └── healthmer
│   │   │   │               ├── HealthMerApplication.java
│   │   │   │               ├── config
│   │   │   │               │   ├── DBConfig.java
│   │   │   │               │   ├── SecurityConfig.java
│   │   │   │               │   └── WebConfig.java
│   │   │   │               ├── controller
│   │   │   │               │   ├── AuthController.java
│   │   │   │               │   ├── CategorySelectingController.java
│   │   │   │               │   ├── TimerController.java
│   │   │   │               │   └── UserController.java
│   │   │   │               ├── interceptor
│   │   │   │               │   └── BearerTokenInterceptor.java
│   │   │   │               ├── model
│   │   │   │               │   ├── dao
│   │   │   │               │   │   ├── AuthDao.java
│   │   │   │               │   │   ├── CategorySelectingDao.java
│   │   │   │               │   │   ├── TimerDao.java
│   │   │   │               │   │   └── UserDao.java
│   │   │   │               │   ├── dto
│   │   │   │               │   │   ├── ChangePasswordRequest.java
│   │   │   │               │   │   ├── HealthCategory.java
│   │   │   │               │   │   ├── Routine.java
│   │   │   │               │   │   ├── SearchCondition.java
│   │   │   │               │   │   ├── Timer.java
│   │   │   │               │   │   ├── TimerCategory.java
│   │   │   │               │   │   ├── TimerRequest.java
│   │   │   │               │   │   └── User.java
│   │   │   │               │   ├── service
│   │   │   │               │   │   ├── AuthService.java
│   │   │   │               │   │   ├── AuthServiceImpl.java
│   │   │   │               │   │   ├── CategorySelectingService.java
│   │   │   │               │   │   ├── TimerService.java
│   │   │   │               │   │   ├── TimerServiceImpl.java
│   │   │   │               │   │   ├── UserService.java
│   │   │   │               │   │   └── UserServiceImpl.java
│   │   │   │               └── util
│   │   │   │                   └── JwtUtil.java
│   │   │   └── resources
│   │   │       ├── Mappers
│   │   │       │   ├── AuthMapper.xml
│   │   │       │   ├── CategorySelectingMapper.xml
│   │   │       │   ├── TimerMapper.xml
│   │   │       │   └── UserMapper.xml
│   │   │       └── application.properties
│   │   └── test
│   │       └── java
│   │           └── com
│   │               └── minijean
│   │                   └── healthmer
│   │                       └── HealthMerApplicationTests.java
│   └── target
```



## 6.실행화면
<!-- 
| |  | |
| :--------: | :--------: | :--------: |
| <img src = "" height = "600"> | <img src="" height = "600"> | |
-->

## 7.트러블 슈팅
## 8.프로젝트 수행 중 핵심 경험
---
[🔝 맨 위로 이동하기](#HealthMer)

