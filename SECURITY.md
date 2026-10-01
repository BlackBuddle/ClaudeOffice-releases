# 보안 정책 (Security Policy)

## 지원하는 버전

보안 수정은 [최신 릴리스](https://github.com/BlackBuddle/ClaudeOffice-releases/releases/latest)에만 반영해요. 설치형은 자동 업데이트(기본 켬)로 최신 릴리스를 받아요. 휴대용은 새 버전 알림만 와서 직접 받아야 해요.

## 취약점 신고

대화 내용이 새어 나가거나, 로컬 서버(`127.0.0.1`)를 다른 사이트에서 악용하거나, 사용자 뜻과 다른 글이 다른 세션에 전달되거나, 자동 업데이트를 속이는 것처럼 보호를 무너뜨리는 문제는 **공개 이슈에 올리지 말고** [비공개 취약점 신고](https://github.com/BlackBuddle/ClaudeOffice-releases/security/advisories/new)로 알려 주세요. 신고 내용은 공개되지 않아요.

이런 문제를 알려 주세요.

- 다른 사이트(웹 페이지)에서 로컬 서버의 대화 전문·세션 목록을 읽거나 명령 대기열에 글을 넣을 수 있는 방법(DNS 리바인딩, 교차 사이트 요청 등)
- 다른 사이트나 다른 기기에서 [보내기]·관제탑 경로로 사용자가 보내지 않은 글이 세션에 전달되게 하는 방법, 또는 전달한 글이 승인으로 오인되게 하는 방법
- 자동 업데이트의 검증(SHA-256 확인)을 건너뛰거나 다른 파일을 설치시키는 방법
- 설치·제거 프로그램이 의도하지 않은 위치나 권한으로 파일을 쓰거나 지우게 하는 방법
- 대화 내용·비밀 정보가 의도하지 않은 곳(로그, 캐시, 네트워크)으로 새는 경우

신고에 다음을 담아 주시면 확인이 빨라요.

- ClaudeOffice 버전 (Windows **설정 → 앱 → 설치된 앱**, 또는 `%APPDATA%\ClaudeOffice\app.log`의 "시작 v…" 줄)
- Windows 버전
- 재현 순서와 영향

**대화 내용, 세션 이름, 파일 경로, 키·비밀번호는 지우고** 알려 주세요(`app.log`에도 경로가 들어 있을 수 있어요).

코드 서명이 없는 것, 로컬 서버에 로그인이 없어서 같은 PC의 다른 프로그램이 접근할 수 있는 것, 자동 업데이트가 저장소 계정 탈취 같은 공급망 위험을 막지 못하는 것처럼 README의 [알려진 한계](README.md#알려진-한계)에 적힌 것은 이미 알고 있는 내용이라 따로 신고하지 않으셔도 돼요. 다만 그 한계를 넘어서는 방법(예: 다른 사이트에서 서버를 악용)을 찾으셨다면 알려 주세요.

최선을 다해 살펴보지만, 처리 시점과 결과를 약속하지는 않아요.

## 배포 파일 확인

공식 배포처는 이 저장소의 **Releases뿐**이에요. 받은 파일의 SHA-256이 같은 릴리스의 `.sha256` 파일에 적힌 값과 같은지 확인하세요([설치](README.md#설치)).

```powershell
(Get-FileHash .\ClaudeOffice-Setup-1.0.0.exe -Algorithm SHA256).Hash
```

해시가 다르거나 다른 곳에서 받은 파일은 실행하지 마세요. 변조된 배포물을 발견하면 위의 비공개 신고로 알려 주세요. 설치 파일에는 코드 서명이 없어서 처음 실행할 때 Windows SmartScreen 경고가 떠요. 해시를 확인한 파일만 **추가 정보 → 실행**을 누르세요.

## English

Please report security issues privately through
[GitHub private vulnerability reporting](https://github.com/BlackBuddle/ClaudeOffice-releases/security/advisories/new),
not through public issues. Examples: reading conversations or the session list from another website through the local server (DNS rebinding, cross-site requests), putting text into the command queue or having text relayed to another session that the user did not send, bypassing the automatic update's SHA-256 check, installer/uninstaller writing or deleting files at unintended locations, or conversation content and secrets leaking into logs, caches or the network. Please include the ClaudeOffice version, the Windows version and the steps to reproduce, and remove conversation content, session names, file paths and keys. The items listed in the README's [Known limitations](README.md#알려진-한계) (no code signature, no login on the local server so other programs on the same PC can reach it, supply-chain risk of automatic updates) are already known.

Only the latest release receives fixes. The only official downloads are this repository's Releases; verify the file's SHA-256 against the `.sha256` asset before running it. The installer has no code signature, so SmartScreen may warn on first run.
