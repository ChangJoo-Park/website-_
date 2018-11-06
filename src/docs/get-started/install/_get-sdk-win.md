## Flutter SDK 내려받기

 1. 아래에서 가장 최신에 릴리즈된 Flutter SDK를 내려받으세요.

    [(loading...)](#){:.download-latest-link-{{os}}.btn.btn-primary}

    다른 릴리즈 버전이나 이전 버전 빌드를 받으려면 [SDKarchive](/docs/development/tools/sdk/archive) 페이지를 방문하세요.

 1. 원하는 위치에 `flutter` 라는 디렉터리 이름으로 zip 파일을 압축을 푸세요. 
    (예: `C:\src\flutter`; `C:\Program Files\`에는 맞지 않습니다.)

 1. `flutter` 디렉터리 안에 있는 `flutter_console.bat` 파일을 실행하세요.

Flutter 커맨드를 Flutter 콘솔에서 사용할 준비가 끝났습니다!

현재 사용중인 버전을 업데이트하려면, [Flutter 업그레이드](/docs/development/tools/sdk/upgrading)를 참조하세요.

### 경로 업데이트

보통의 다른 윈도우 터미널에서 Flutter 명령어를 사용하려면 `PATH` 환경변수에 Flutter를 추가하세요

* 시작 버튼의 검색창에서 '환경'를 입력하고 **시스템 환경변수 편집** 을 선택하세요.
* **사용자 변수** 에서 **Path** 를 선택하세요:
  * Path가 있으면 전체 내용의 끝에 `;`과 함께 전체 경로의 `flutter\bin`을 추가하세요.
  * `Path`가 없으면 새로 만든 후 전체 경로의 `flutter\bin` 를 입력하세요.

위 변경사항을 적용하려면 기존 명령 프롬프트 등을 닫은 후 다시 열어야 합니다.

### `flutter doctor` 실행하기

터미널에서 Flutter SDK 경로로 들어가 아래 명령어를 실행하여 설치에 필요한 의존성을 확인합니다.

```console
C:\src\flutter>flutter doctor
```

이 명령어는 현재 환경에서 Flutter 설치 상태 리포트를 보여줍니다. 추가로 설치할 소프트웨어가 있는지 확인하고 추가 작업을 해야합니다. (**굵은** 텍스트 참조).

사용 예:

<pre>
[-] Android toolchain - develop for Android devices
    • Android SDK at D:\Android\sdk
    <strong>✗ Android SDK is missing command line tools; download from https://goo.gl/XxQghQ</strong>
    • Try re-installing or updating your Android SDK,
      visit https://flutter.io/setup/#android-setup for detailed instructions.
</pre>

`flutter doctor` 를 이용해 설치 프로세스를 완료하는 방법을 알려줍니다. 

{% include_relative _analytics.md %}
