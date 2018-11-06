## iOS 설치하기

### Xcode 설치

iOS를 위한 Flutter 앱 개발을 위해 Xcode 9.0 이상을 지원하는 Mac이 필요합니다.

 1. Xcode 9.0 버전 이상을 설치합니다. [웹에서 다운로드](https://developer.apple.com/xcode/) 또는 [Mac App Store](https://itunes.apple.com/us/app/xcode/id497799835)를 이용하세요.
 1. 새 버전 Xcode를 설치했다면 Xcode command-line tools를 설정하세요.
    ```terminal
    $ sudo xcode-select --switch /Applications/Xcode.app/Contents/Developer
    ```

    최신 버전 Xcode를 설치했다면 대부분의 경우에 올바른 경로입니다.
    다른 버전을 사용한다면 해당 경로로 변경해야합니다.

 1. Xcode 라이센스 동의를 하려면 Xcode를 실행하거나 터미널에서 `sudo xcodebuild -license` 를 입력하세요.

Xcode를 이용하면 Flutter 앱을 iOS 디바이스 또는 시뮬레이터에서 실행할 수 있습니다.

### iOS 시뮬레이터 설정하기

Flutter 앱을 iOS 시뮬레이터에서 실행하고 테스트하기 위해 아래 과정이 필요합니다.

 1. Mac에서 Spotlight 또는 아래 명령어로 시뮬레이터를 실행하세요.
    ```terminal
    $ open -a Simulator
    ```

 2. 아이폰 5s 이후의 디바이스에서 64비트로 실행하기 위해 시뮬레이터의 **Hardware > Device** 메뉴를 선택합니다.
 3. 개발하는 디바이스의 화면 크기에 따라 시뮬레이터가 화면보다 클 수 있습니다 **Window > Scale** 메뉴에서 조정하세요.
 4. `flutter run` 명령어로 앱을 실행하세요.

### iOS 디바이스에 배포하기

Flutter 앱을 실제 iOS 디바이스에 배포하기 위해 몇개의 추가 도구와 애플 계정이 필요합니다.

 1. [homebrew](http://brew.sh/)를 설치하세요.
 1. 터미널을 열어 아래의 명령어를 실행하세요

    ```terminal
    $ brew update
    # The following two steps are a temporary workaround to https://github.com/flutter/flutter/issues/22595
    $ brew install --HEAD usbmuxd
    $ brew link usbmuxd
    $ brew install --HEAD libimobiledevice
    $ brew install ideviceinstaller ios-deploy cocoapods
    $ pod setup
    ```

   실행하는데 오류가 발생하면 `brew doctor` 명령어로 해결할 수 있습니다.

 1. Xcode 사이닝 절차를 따라가면 프로젝트를 프로비저닝할 수 있습니다.

     {: type="a"}

     1. Xcode 워크스페이스를 열고 `ios/Runner.xcworkspace` 를 터미널에서 실행하세요.
     1. Xcode에서 `Runner` 프로젝트를 왼쪽 네비게이션 패널에서 선택하세요.
     1. `Runner` 타겟 설정 페이지에서 Development Team이  **General > Signing > Team** 에 있는지 확인하세요.
        팀을 선택하면 Xcode는 계정에 할당된 개발자 인증서를 만들고 내려받습니다. 그리고 필요한 경우 프로필 프로비저닝을 합니다.

        * 첫번째 iOS 개발 프로젝트를 한다면 Xcode에서 애플 ID로 로그인 해야합니다.
          <br>
          ![Xcode account add](/images/setup/xcode-account.png)
          <br>
          개발과 테스트에는 애플 ID가 필요합니다. 애플 개발자 프로그램에 등록되어 있어야합니다.
          [맴버십 선택하기](https://developer.apple.com/kr/support/compare-memberships/)를 확인하세요.

        * 처음 실제 iOS 디바이스를 연결하면 인증 다이얼로그가 출력됩니다. `신뢰함` 을 선택하세요.

          ![Trust Mac](/images/setup/trust-computer.png)

          이제 iOS 기기의 설정에서 **일반 > 기기 관리** 에서 신뢰한 앱 목록을 확인할 수 있습니다.

        * 자동 사이닝에 실패하면 프로젝트에서 **General > Identity > Bundle Identifier** 의 값이 유니크 값인지 확인하세요.
          <br>
          ![Check the app's Bundle ID](/images/setup/xcode-unique-bundle-id.png)

 1. `flutter run` 명령어로 앱을 실행하세요.
