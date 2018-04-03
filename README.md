# Fabric

테스트용 어플을 만들고 이런 저런 테스트를 하다보면 오류가 발생되어 비정상 종료가 발생한다. 마침 USB 디버깅 중이었다면 자연스럽게 로그캣을 확인하면 될테지만, 그렇지 않은 상황에서는 오류의 원인을 찾을 수 없다. 이러한 불편함을 해소하기 위해 어플 크래시 분석 라이브러리인 Fabric을 소개한다.

## 1. 플러그인 설치

계정이 생성된 이후엔 프로젝트를 동기화 시켜야 한다.

Preference -> Plugins로 이동한 후

![preference plugins](https://github.com/Ekutz/Fabric/blob/master/preference%20plugins.png?raw=true)

Fabric을 검색하여 설치한다.

![fabric plugin](https://github.com/Ekutz/Fabric/blob/master/fabric%20plugin.png?raw=true)

## 3. 가입 및 로그인

Fabric plugin이 정상적으로 설치되었다면 스튜디오 우측 상단에 있는 Fabric을 눌러 플러그인을 열어 sign up을 눌러 가입한다.

![open fabric](https://github.com/Ekutz/Fabric/blob/master/open%20fabric.png?raw=true)

![sign up](https://github.com/Ekutz/Fabric/blob/master/sign%20up.png?raw=true)

## 4. 조직 생성

메일을 통해 컨펌을 받고 나면 조직을 생성할 수 있다. 적당한 이름을 가진 조직을 생성해보자.

![organize](https://github.com/Ekutz/Fabric/blob/master/organize.png?raw=true)

## 5. 플랫폼 선택

조직을 생성한 뒤에는 Fabric을 사용할 플랫폼을 선택해야 한다. 이 포스트는 안드로이드 관련 포스트이기 때문에 Android를 선택한다.

![platform](https://github.com/Ekutz/Fabric/blob/master/platform.png?raw=true)

## 6. 프로젝트 동기화

모든 준비가 끝나면 플러그인에 로그인을 한 후 프로젝트를 동기화 시킨다.

로그인 후 조직을 선택하고

![check team](https://github.com/Ekutz/Fabric/blob/master/check%20team.png?raw=true)

각종 어플 오류를 분석하기 위한 Crashlytics를 선택한다.

![add crashlytics](https://github.com/Ekutz/Fabric/blob/master/add%20crashlytics.png?raw=true)

다음 화면으로 넘어간 후 Crashlytics를 install 한다.

![install](https://github.com/Ekutz/Fabric/blob/master/install.png?raw=true)

그러면 화면이 다음과 같이 변하고 apply만 누르면 모든 세팅이 자동으로 설정된다.

![auto modify](https://github.com/Ekutz/Fabric/blob/master/auto%20modify.png?raw=true)

아래와 같은 화면이 나온다면 성공적으로 진행된 것이다.

![last](https://github.com/Ekutz/Fabric/blob/master/last.png?raw=true)

이제 어플을 빌드하고 동작시킨다면 Fabric.io dashboard에 자동으로 어플이 등록된다.

이제 [Fabric 로그인 화면](https://fabric.io/login)으로 이동하여 로그인을 하면 dashboard에 어플이 등록된 것을 확인할 수 있다.

![dashboard](https://github.com/Ekutz/Fabric/blob/master/dashboard.png?raw=true)

웹 페이지 좌측의 Crashlytics를 선택하면 이제 usb 디버깅 없이 편리하게 오류를 수집할 수 있게 되었다.

![final](https://github.com/Ekutz/Fabric/blob/master/final.png?raw=true)

## 7. 포스트를 마무리하며...

단순한 USB 디버거 대용으로 생각하기 보단 사용자 데이터 수집기로 생각하는 것이 더 좋을 것 같다. 여러 환경에서 테스트를 직접 진행할 순 없는데 이를 OS, 기기, 버젼에 따라 다르게 수집해 주는 훌륭한 툴이다. 되도록 프로젝트 제작 초창기에 투입하여 최대한 많은 오류를 잡을 수 있으면 좋겠다.
