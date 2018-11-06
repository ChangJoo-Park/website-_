---
title: 윈도우에 설치
short-title: Windows
# js: [{defer: true, url: /assets/archive.js}]
next:
  title: Set up an editor
  path: /get-started/editor
---

{% assign os = 'windows' -%}

## 시스템 요구사항

Flutter를 설치하고 실행하기 위해 아래의 최소 개발환경 요구사항을 충족해야합니다.

- **운영체제**: Windows 7 SP1 이상 (64-bit)
- **디스크 잔여 공간**: 400 MB (IDE나 기타 개발도구 제외).
- **개발 도구**: Flutter를 사용하는 환경에 따라 다른 개발 도구가 필요합니다.
  - [Windows PowerShell 5.0][] 또는 최신 버전 (Windows 10에 기본 내장)
  - [Git for Windows][], **Use Git from the Windows Command Prompt** 옵션으로 설치되어있어야 합니다..

     Git for Windows가 이미 설치되어 있다면, `git` 명령어를 명령 프롬프트 또는 PowerShell에서 실행해보세요. 

{% include_relative _get-sdk-win.md %}

{% include_relative _android-setup.md %}

## 다음 단계로

[다음 단계: 에디터 설정](/get-started/editor)

[Git for Windows]: https://git-scm.com/download/win
[Windows PowerShell 5.0]: https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-windows-powershell
