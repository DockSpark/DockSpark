# DockSpark

[English](README.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Español](README.es.md)

DockSpark를 사용하면 macOS Dock에서 바로 브라우저 프로필을 전환할 수 있습니다. 지원하는 브라우저 아이콘 위에 포인터를 올린 다음 원하는 프로필을 선택하세요. 브라우저의 프로필 메뉴를 열 필요가 없습니다.

[최신 버전 다운로드](https://github.com/DockSpark/DockSpark/releases/latest)
· [공식 웹사이트](https://dockspark.app)
· [변경 내역(영어)](CHANGELOG.md)
· [문제 신고](https://github.com/DockSpark/DockSpark/issues)

## 기능

- 브라우저의 Dock 아이콘에 표시되는 팝오버에서 프로필 전환
- 네이티브 macOS 앱에서 브라우저 프로필 관리
- 이름과 색상을 지정하여 프로필을 빠르게 구분
- Dock 호버 메뉴에 표시할 이름 있는 프로필 선택
- DockSpark Free 사용 또는 Pro로 브라우저 및 프로필 수 제한 해제
- 메뉴 막대 아이콘과 Dock 아이콘 표시 또는 숨기기
- 앱 내에서 업데이트 확인
- 도움말 메뉴에서 문서 열기 또는 정해진 양식으로 피드백 보내기
- 영어, 중국어 간체, 중국어 번체, 일본어, 한국어, 독일어, 프랑스어, 스페인어 지원
- Dock 아이콘 크기에 맞춰 팝오버 크기 조정(Dock 확대 효과 포함)
- 일반 설정에서 익명 사용 분석 끄기

## 시스템 요구 사항

- macOS 14.0 이상
- Apple Silicon 또는 Intel Mac
- 지원하는 브라우저를 Dock에 유지

### 지원 브라우저

| 브라우저 | Dock에서 프로필 전환 |
| --- | --- |
| Safari | 지원 |
| Firefox | 지원 |
| Google Chrome | 지원 |
| Chromium | 지원 |
| Microsoft Edge | 지원 |
| Brave Browser | 지원 |
| Vivaldi | 지원 |
| Opera | 지원 |
| Opera GX | 지원 |
| Arc | 지원 |

Safari, Google Chrome, Firefox는 설치되어 있으면 기본으로 활성화됩니다. Free 요금제에서는 브라우저 하나를 활성화할 수 있으며, 브라우저당 이름 있는 프로필을 세 개까지 사용할 수 있습니다. 개인정보 보호 브라우징 및 시크릿 모드 항목은 프로필 수 제한에 포함되지 않습니다. Pro는 이러한 제한을 해제합니다. 다른 설치된 브라우저는 앱 목록에서 추가할 수 있습니다.

## 설치

### Homebrew

```sh
brew trust --cask dockspark/tap/dockspark && \
  brew install --cask dockspark/tap/dockspark
```

### 직접 다운로드

1. [최신 릴리스](https://github.com/DockSpark/DockSpark/releases/latest)를 엽니다.
2. `DockSpark-0.5.0.dmg`를 다운로드합니다. GitHub에서 자동 생성한 소스 코드 압축 파일은 다운로드하지 마세요.
3. 디스크 이미지를 열고 `DockSpark.app`을 응용 프로그램 폴더로 드래그합니다.
4. DockSpark를 실행하고 요청하는 macOS 권한을 허용합니다.

수동 설치용 `DockSpark-0.5.0.zip` 파일도 제공됩니다.

DockSpark는 Developer ID 인증서로 서명되었으며 Apple의 공증을 받았습니다.

## 권한

DockSpark는 프로필 전환에 필요한 시스템 권한만 요청합니다.

- **손쉬운 사용**: Dock에 있는 지원 브라우저 아이콘과 포인터의 상호 작용을 감지합니다.
- **자동화**: DockSpark가 선택한 브라우저에 프로필 전환을 요청할 수 있도록 합니다.
- **전체 디스크 접근 권한**: 선택 사항입니다. Chromium 및 Firefox 프로필의 메타데이터를 찾는 데만 사용합니다.

**시스템 설정 > 개인정보 보호 및 보안**에서 언제든지 권한을 확인하거나 취소할 수 있습니다.

## 사용 방법

1. 지원하는 브라우저를 Dock에 추가합니다.
2. DockSpark에서 브라우저와 프로필을 설정합니다.
3. 브라우저의 Dock 아이콘 위에 포인터를 올립니다.
4. 팝오버에서 프로필을 선택합니다.

## AI 어시스턴트 스킬

[DockSpark 스킬](skills/dockspark/SKILL.md)은 AI 어시스턴트가 DockSpark의 기능과 활용 상황을 설명하고, 설치 및 일상적인 사용을 안내하고, 공식 문서를 찾고, 일반적인 문제를 해결하도록 돕습니다. 스킬 버전 **0.5.0**은 앱 버전에 맞춰 관리되며, 포함된 안내는 DockSpark 0.5.0을 기준으로 검토되었습니다. 어시스턴트는 사용자의 언어로 답변합니다.

[Skills CLI](https://github.com/vercel-labs/skills)로 설치합니다(Node.js가 필요하며, 현재 요구 사항은 CLI 문서를 참고하세요).

```sh
npx skills add DockSpark/DockSpark --skill dockspark
```

안내에 따라 AI 어시스턴트를 선택하세요. 기본적으로 현재 프로젝트에 설치되며, 전역 설치에는 `-g`를 추가합니다. 위 GitHub 명령을 사용하려면 스킬이 이 저장소에 게시되어 있어야 합니다. 로컬 체크아웃에서 설치할 때는 다음 명령을 사용하세요.

```sh
npx skills add . --skill dockspark
```

[Codex에 수동 설치](https://developers.openai.com/codex/skills/)하려면 `references/`와 `agents/`를 포함한 `skills/dockspark` 디렉터리 전체를 `~/.agents/skills/dockspark` 또는 프로젝트의 `.agents/skills/dockspark`로 복사하세요. 다른 어시스턴트는 다른 스킬 디렉터리를 사용할 수 있습니다. 스킬이 표시되지 않으면 어시스턴트의 스킬을 다시 로드하거나 새 세션을 시작하세요.

프롬프트 예시:

- `$dockspark를 사용해서 DockSpark로 무엇을 할 수 있는지 설명해 줘.`
- `$dockspark를 사용해서 Chrome 프로필 설정을 도와줘.`
- `$dockspark를 사용해서 Dock 아이콘 위에 포인터를 올려도 반응이 없는 원인을 찾아줘.`

영어나 다른 언어로도 질문할 수 있습니다. 스킬은 사용 안내를 제공하며, 앱을 사용하려면 DockSpark를 별도로 설치해야 합니다. 새 앱 버전을 출시할 때마다 스킬 안내와 공식 링크를 검토하고, 스킬 버전과 검토 기준 앱 버전을 함께 업데이트하세요.

## 스크린샷

![DockSpark 프로필 관리 창](Assets/img_dockspark.jpg)

> DockSpark 인터페이스를 보여 주는 스크린샷입니다. 버전 0.5.0은 Safari, Firefox, Chrome 및 위 표에 나열된 다른 Chromium 기반 브라우저의 Dock 프로필 전환을 지원합니다.

## 업데이트

DockSpark는 Sparkle을 사용하여 앱 내 업데이트를 제공합니다. [릴리스 페이지](https://github.com/DockSpark/DockSpark/releases)에서 직접 다운로드할 수도 있습니다.

## 릴리스 파일 무결성

SHA-256 체크섬은 다음과 같습니다.

```text
DockSpark-0.5.0.dmg  90c0f9369d67eb33e6939b1cac008ec70277f7c176c0f2a1aa0e50fb08e85eff
DockSpark-0.5.0.zip  1d7eb10b9ce7736f2a1e5f1fd790eebb399675fadb95702a6032f329f65db129
```

다운로드 후 다음 명령으로 확인하세요.

```sh
shasum -a 256 DockSpark-0.5.0.dmg DockSpark-0.5.0.zip
```

## 피드백

[GitHub Issues](https://github.com/DockSpark/DockSpark/issues)에서 버그를 신고하거나 개선 사항을 제안해 주세요. 버그 신고 시 macOS 버전, 브라우저 버전, 재현 단계를 함께 적어 주세요.

이 저장소에는 DockSpark의 공개 릴리스 자료가 포함되어 있습니다. 앱 소스 코드는 포함되어 있지 않습니다.
