---
title: Linux install
short-title: Linux
# js: [{defer: true, url: /assets/archive.js}]
next:
  title: Set up an editor
  path: /get-started/editor
---

{% assign os = 'linux' -%}

## 시스템 요구사항

Flutter를 설치하고 실행하기 위해 아래의 최소 개발환경 요구사항을 충족해야합니다.


- **운영체제**: Linux (64-bit)
- **디스크 잔여 공간**: 600 MB (does not include disk space for IDE/tools).
- **개발 도구**: Flutter를 사용하는 환경에 따라 다른 개발 도구가 필요합니다.
  - `bash`, `mkdir`, `rm`, `git`, `curl`, `unzip`, `which`
- **라이브러리**: Flutter의 `test` 명령어는 아래 라이브러리가 필요합니다.
  - `libGLU.so.1` - mesa 패키지에서 제공됩니다. Ubuntu/Debian의 경우 `libglu1-mesa`  

{% include_relative _get-sdk.md %}

{% include_relative _path-mac-linux.md %}

{% include_relative _android-setup.md %}

## 다음 단계로

[다음 단계: 에디터 설정](/get-started/editor)
