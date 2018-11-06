## 안드로이드 설치하기

{{site.alert.note}}
  Flutter relies on a full installation of Android Studio to supply
  its Android platform dependencies. However, you can write your
  Flutter apps in a number of editors; a later step will discuss that.
{{site.alert.end}}

### 안드로이드 스튜디오 설치하기

 1. [안드로이드 스튜디오](https://developer.android.com/studio/index.html)를 다운로드하고 설치하세요.
 1. 안드로이드 스튜디오를 실행하고, 'Android Studio Setup Wizard'를 진행합니다.
    이를 통해 최신 Android SDK와 Android SDK Platform-Tools, 그리고 Android SDK Build-Tools 등의
    안드로이드를 위한 Flutter를 개발하는데 필요한 개발 도구를 설치합니다.

### 안드로이드 디바이스 설정하기

Flutter 앱을 실행하고 테스트하려면, 안드로이드 4.1 (API 레벨 16) 또는 그 이상의 버전이 설치된 디바이스가 필요합니다.

 1. 디바이스에서 **개발자 옵션** 과 **USB 디버그** 를 활성화하세요. 자세한 내용은 [안드로이드 문서](https://developer.android.com/studio/debug/dev-options.html)에 있습니다.
 1. 윈도우 사용자라면 : [Google USB Driver](https://developer.android.com/studio/run/win-usb)를 설치하세요.
 1. USB 케이블로 디바이스와 컴퓨터를 연결하세요. 조금 기다리면 컴퓨터가 디바이스에 접근 권한을 요청합니다.
 1. 터미널에서, `flutter devices` 명령어를 이용해 Flutter가 연결된 기기를 감지하는지 확인하세요.

기본적으로, Flutter는 설치된 Android SDK의 `adb` 를 이용합니다. Flutter가 다른 버전의 Android SDK를 사용하도록 하려면, `ANDROID_HOME` 환경변수를 설치된 디렉터리로 지정하세요.

### 안드로이드 에뮬레이터 설정하기

안드로이드 에뮬레이터에서 Flutter 앱을 실행하고 테스트하려면 아래 순서를 따라하세요.

 1. [VM acceleration](https://developer.android.com/studio/run/emulator-acceleration.html)을 활성화하세요.
 1. **Android Studio > Tools > Android > AVD Manager** 메뉴를 따라가 **Create Virtual Device**를 선택하세요.
    (**Android** 서브메뉴는 안드로이드 프로젝트인 경우에만 볼 수 있습니다.)
 1. 사전 정의된 기기를 선택하고 **Next** 를 누르세요.
 1. 사용을 원하는 하나 또는 그 이상의 안드로이드 시스템 버전을 선택하고, **Next** 를 누르세요. _x86_ 또는 _x86\_64_ 이미지를 추천합니다.
 1. Emulated Performance에서 **Hardware - GLES 2.0** [하드웨어 가속](https://developer.android.com/studio/run/emulator-acceleration.html)을 활성화하세요.
 1. AVD 설정이 맞는지 확인하고 **Finish** 를 선택하세요.
    위 내용의 자세한 설명은 [Managing AVDs](https://developer.android.com/studio/run/managing-avds.html)를 참조하세요.
 1. Android Virtual Device Manager에서 툴바의 **Run** 을 클릭하세요.
    선택한 OS 버전과 기기로 에뮬레이터가 시작됩니다.
