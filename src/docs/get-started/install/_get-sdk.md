{% if os == 'linux' -%}
  {% assign unzip = 'tar xf' -%}
  {% assign file_ext = '.tar.xz' -%}
{% else -%}
  {% assign unzip = 'unzip' -%}
  {% assign file_ext = '.zip' -%}
{% endif -%}

## Flutter SDK 내려받기 {#get-sdk}

 1. 아래에서 가장 최신에 릴리즈된 Flutter SDK를 내려받으세요.

    [(loading...)](#){:.download-latest-link-{{os}}.btn.btn-primary}

    다른 릴리즈 버전이나 이전 버전 빌드를 받으려면 [SDKarchive](/docs/development/tools/sdk/archive) 페이지를 방문하세요.

 1. 원하는 경로에 압축을 풀어주세요.
    
    사용 예:

    {% comment %}
      Our JS also updates the filename in this template, but it doesn't include the terminal formatting:

      {% prettify shell %}
      $ cd ~/development
      $ {{unzip}} ~/Downloads/[[download-latest-link-filename]]flutter_{{os}}_vX.X.X-beta{{file_ext}}[[/end]]
      {% endprettify %}
    {% endcomment -%}

    ```terminal
    $ cd ~/development
    $ {{unzip}} ~/Downloads/flutter_{{os}}_vX.X.X-beta{{file_ext}}
    ```

 1. `flutter` 도구를 PATH에 추가하세요

    ```terminal
    $ export PATH=$PATH:`pwd`/flutter/bin
    ```

위 명령어를 입력하면 `PATH` 환경변수에 현재 터미널 윈도우에 한하여 임시로 추가됩니다. 지속적으로 추가하려면 [경로 설정](#update-your-path)을 확인하세요.

이제 Flutter 명령어를 쓸 수 있습니다!

현재 사용중인 버전을 업데이트하려면, [Flutter 업그레이드](/docs/development/tools/sdk/upgrading)를 참조하세요.

### `flutter doctor` 실행하기

다음 명령어를 이용해 설치를 마무리하세요.

```terminal
$ flutter doctor [-v]
```

이 명령어는 현재 환경에서 Flutter 설치 상태 리포트를 보여줍니다. 추가로 설치할 소프트웨어가 있는지 확인하고 추가 작업을 해야합니다. (**굵은** 텍스트 참조).

사용 예:

<pre>
[-] Android toolchain - develop for Android devices
    • Android SDK at /Users/obiwan/Library/Android/sdk
    <strong>✗ Android SDK is missing command line tools; download from https://goo.gl/XxQghQ</strong>
    • Try re-installing or updating your Android SDK,
      visit https://flutter.io/setup/#android-setup for detailed instructions.
</pre>

`flutter doctor` 를 이용해 설치 프로세스를 완료하는 방법을 알려줍니다. 

{% include_relative _analytics.md %}
