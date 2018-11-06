---
title: MacOS install
short-title: MacOS
next:
  title: Set up an editor
  path: /get-started/editor
---

{% assign os = 'macos' -%}

## 시스템 요구사항

Flutter를 설치하고 실행하기 위해 아래의 최소 개발환경 요구사항을 충족해야합니다.

- **운영체제**: macOS (64-bit)
- **디스크 잔여 공간**: 700 MB (IDE나 기타 개발도구 제외).
- **개발 도구**: Flutter를 사용하는 환경에 따라 다른 개발 도구가 필요합니다.
  - `bash`, `mkdir`, `rm`, `git`, `curl`, `unzip`, `which`

{% include_relative _get-sdk.md %}

{% include_relative _path-mac-linux.md %}

## 플랫폼 설치

MacOS에서는 Flutter를 사용하여 iOS와 안드로이드 앱을 모두 개발할 수 있습니다. 두 플랫폼 중 적어도 한 플랫폼은 설치되어있어야 첫번째 Flutter앱을 빌드하거나 실행할 수 있습니다. 

{% include_relative _ios-setup.md %}

{% include_relative _android-setup.md %}

## 다음 단계로

[다음 단계: 에디터 설정](/get-started/editor)
