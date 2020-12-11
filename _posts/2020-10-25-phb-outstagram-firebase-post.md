---
layout: post
title: "안드로이드 스튜디오 파이어베이스 연동하기"
tags: [ParkHanbaek, firebase, kotlin, android studio, 안드로이드 스튜디오 연동하기, 삽질의 흔적]
comments: true
---

# 안드로이드 스튜디오, 파이어베이스 연동하기

안드로이드 스튜디오를 이용해 인스타그램 만들기 시리즈 첫번째 삽질. (사실 두번째)

앞으로 올리게될 모든 게시물은 공부와 동시에 복습을 위해서 작성하기 때문에 부족한 부분이 있을 수 있습니다!

---

## 1. 안드로이드 프로젝트 만들기.

---

따로 설명없이 Empty엑티비티로 프로젝트를 만들어주면 된다.

---

## 2. 안드로이드 스튜디오 프로젝트와 파이어베이스 연동하기.

---



![스크린샷 2020-11-07 오후 6 46 53](https://user-images.githubusercontent.com/43005678/98438653-27cf2b00-212f-11eb-81c5-52894c741e73.png)

구글에 파이어베이스 검색

![스크린샷 2020-11-07 오후 6 49 24](https://user-images.githubusercontent.com/43005678/98438736-885e6800-212f-11eb-97d8-c254a4ee58a4.png)

시작하기 클릭

![스크린샷 2020-11-07 오후 6 49 30](https://user-images.githubusercontent.com/43005678/98460987-362f4c80-21ec-11eb-975f-ac0929abd0fd.png)

프로젝트 추가


![스크린샷 2020-11-07 오후 6 49 44](https://user-images.githubusercontent.com/43005678/98460999-4c3d0d00-21ec-11eb-86b4-bd805d9e6570.png)

이름을 지어줍니다!

![스크린샷 2020-11-07 오후 6 49 47(2)](https://user-images.githubusercontent.com/43005678/98461087-c2417400-21ec-11eb-9982-6cf53deadcf6.png)

Google 애널리틱스 사용 설정 체크

![스크린샷 2020-11-07 오후 6 51 06](https://user-images.githubusercontent.com/43005678/98461117-f6b53000-21ec-11eb-9edf-f8062dd65b7e.png)

애널리틱스 위치 설정하고, 약관 모두 체그해줍니다.

![스크린샷 2020-11-07 오후 6 51 17](https://user-images.githubusercontent.com/43005678/98461137-1d736680-21ed-11eb-84a4-1b1ee426242a.png)

기다려줍니다.

![스크린샷 2020-11-07 오후 6 54 06](https://user-images.githubusercontent.com/43005678/98461143-295f2880-21ed-11eb-9d0c-1497e6f55914.png)

계속.

![스크린샷 2020-11-07 오후 6 54 18](https://user-images.githubusercontent.com/43005678/98461150-367c1780-21ed-11eb-83a4-2f0c77d15086.png)

안드로이드 눌러줍니다.

![스크린샷 2020-11-07 오후 6 58 43](https://user-images.githubusercontent.com/43005678/98461177-5dd2e480-21ed-11eb-852e-7f1b482176b8.png)

패키지 이름은 

![스크린샷 2020-11-07 오후 6 55 05](https://user-images.githubusercontent.com/43005678/98461183-6fb48780-21ed-11eb-94b7-bcc0c767fb23.png)

요거 복사해줍니다.

SHA-1은

![스크린샷 2020-11-07 오후 6 56 40](https://user-images.githubusercontent.com/43005678/98461195-8c50bf80-21ed-11eb-9785-39b0c2ab3bf9.png)

안드로이드 스튜디오에서 터미널 창에 이렇게 입력해줍니다.

![스크린샷 2020-11-07 오후 6 57 40](https://user-images.githubusercontent.com/43005678/98461202-a1c5e980-21ed-11eb-8180-7df475122777.png)

복사 붙여넣기

앱 닉네임은 패스

그 다음 앱 등록 누르고 json파일을 다운받아줍니다.

<img width="187" alt="스크린샷 2020-11-07 오후 6 59 53" src="https://user-images.githubusercontent.com/43005678/98461230-dc2f8680-21ed-11eb-9fc0-19296e0a5dea.png">

복사하기

![스크린샷 2020-11-07 오후 7 00 30](https://user-images.githubusercontent.com/43005678/98461235-eb163900-21ed-11eb-962f-6989c1bbb0f9.png)

복사해서 app파일 안에 붙여넣기 해줍니다.

![스크린샷 2020-11-07 오후 7 01 04](https://user-images.githubusercontent.com/43005678/98461278-3deff080-21ee-11eb-918d-bf80c206497e.png)

다음과 같이 따라 해줍니다.


![스크린샷 2020-11-07 오후 7 01 11](https://user-images.githubusercontent.com/43005678/98461314-7db6d800-21ee-11eb-96e6-d46a1a8524f3.png)

다음과 같이 따라 해줍니다. (2)

```gradle
apply plugin : 'com.android.application'
```
이줄은 다음과 같이 변경 가능합니다.
```gradle
plugins {
    id 'com.android.application'
}
```

<img width="935" alt="스크린샷 2020-11-07 오후 7 02 26" src="https://user-images.githubusercontent.com/43005678/98461492-db97ef80-21ef-11eb-9c3b-613260b70fb6.png">


오른쪽 위에 Sync Now 눌러줍니다.

---
## 3. 끝

안드로이드 스튜디오에서 바로 파이어베이스 연동이 가능하지만, 안드로이드 스튜디오에서 연동이 잘 되지 않는 경우가 있었습니다. 그래서 안드로이드 프로젝트와 파이어베이스 프로젝트를 따로 만들고 연동을 시켜보았습니다!


\
\
이 문서는 아웃스타그램 개발 과정에서 공부한 내용을 바탕으로 작성되었습니다.[아웃스타그램 github 바로가기](https://github.com/totwjfakd/Outstagram)
