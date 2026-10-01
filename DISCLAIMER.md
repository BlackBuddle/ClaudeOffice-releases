# 면책조항과 보안사고 면책 (Disclaimer)

ClaudeOffice 개인 사용 라이선스 v1.0([LICENSE](LICENSE))의 일부예요. 소프트웨어를 쓰기 전에 읽어 주세요. 한국어본과 영어본이 함께 있고, 뜻이 다르면 한국어본이 우선해요.

*This document is part of the ClaudeOffice Personal Use License v1.0 ([LICENSE](LICENSE)). A Korean and an English version are provided; if they differ, the Korean version prevails.*

---

## 한국어

### 1. 있는 그대로 제공해요(무보증)

ClaudeOffice(이하 "소프트웨어")는 **개인 사용자에게 무료로, 있는 그대로("AS IS")** 제공해요. 저작권자는 관련 법령이 허락하는 가장 넓은 범위에서 다음을 포함한 모든 명시적·묵시적 보증을 하지 않아요.

- 오류가 없다는 것, 끊기지 않고 동작한다는 것, 모든 환경(Windows 버전·화면 배율·보안 프로그램·다른 프로그램)에서 동작한다는 것
- 상품성, 특정 목적에 대한 적합성, 제3자의 권리를 침해하지 않는다는 것
- 이 소프트웨어가 보여 주는 정보(세션 상태, 답변·권한 대기 표시, 요약, 사용량·한도·비용, 전달 결과)가 정확하거나 완전하다는 것

### 2. 책임의 제한

관련 법령이 허락하는 가장 넓은 범위에서, 저작권자는 소프트웨어를 쓰거나 쓰지 못해서 생긴 **직접·간접·특별·결과적 손해**(데이터 손실, 파일의 수정·삭제, 이익 손실, 업무 중단, 계정 정지나 불이익, 뜻하지 않은 요금, 기기 고장 등)에 대해 책임을 지지 않아요. 소프트웨어는 무료이므로, 책임이 인정되더라도 그 한도는 사용자가 저작권자에게 낸 금액(0원)으로 해요.

다만 **저작권자의 고의 또는 중대한 과실로 생긴 손해**와 **법령상 배제할 수 없는 책임**(소비자 보호 관련 법령 등)은 이 조항에서 제외해요.

### 3. 보안사고 면책

#### 3.1 이 소프트웨어가 하는 일(알아 두세요)

README의 "개인정보와 보안"에 자세히 적혀 있고, 핵심은 이래요.

- **대화 기록을 읽어요.** 세션을 화면에 보여 주고 요약하려고 Claude Code가 이 PC에 남긴 파일(`~/.claude`의 실행 중 세션 목록, 대화 기록, 서브에이전트 기록, 세션 제목, 토큰 사용량, 그리고 Claude 데스크톱 앱의 세션 파일)을 읽어요. 읽기만 하고 고치지 않아요. 하지만 **대화에는 비밀번호·키·개인정보·회사 기밀이 들어 있을 수 있고, 소프트웨어는 그 내용을 화면(전문 보기 포함)에 그대로 보여 줘요.** `sk-…`, `ghp_…`, `password=…` 같은 비밀 패턴은 가리지만 **완전하지 않아요.** 화면을 다른 사람에게 보여 주거나 캡처·녹화·공유할 때는 사용자가 확인해야 해요.
- **캐시와 기록이 남아요.** 데이터 폴더(`%APPDATA%\ClaudeOffice`)에 세션 제목, 대화 발췌, 보낸 명령 글, 요약이 든 캐시와 기록이 남아요. 앱을 지워도 이 폴더는 남아요.
- **로컬 서버에는 로그인이 없어요.** 서버는 `127.0.0.1`에만 열려 있어서 다른 기기에서는 접근할 수 없어요. 하지만 암호나 로그인이 없어서 **같은 PC에서 도는 다른 프로그램(악성 프로그램 포함)과 같은 PC의 다른 Windows 사용자 계정**이 세션 목록과 대화 전문을 읽거나 명령 대기열에 글을 넣을 수 있어요. 낯선 Host 이름의 요청과, 명령·대화 전문·요약 요청 중 다른 사이트(웹 페이지)에서 온 것은 막지만, 이것이 같은 PC의 프로그램까지 막아 주지는 않아요.
- **[보내기]로 전달한 글은 실제 작업을 일으킬 수 있어요.** 관제탑 세션이 글을 다른 Claude 세션에 전달하면, 받는 세션의 권한 설정에 따라 **파일 수정·삭제, 명령 실행, 외부 전송** 같은 실제 작업이 일어날 수 있어요. 전달한 글은 사용자의 승인이 아니라 다른 세션의 요청으로 취급되지만, 받는 세션이 허용 규칙·auto 모드·`bypassPermissions` 등으로 승인 없이 일하도록 설정돼 있으면 사용자가 보지 않는 사이에 일이 진행될 수 있어요. 어떤 글을 보냈는지, 받는 세션을 어떻게 설정했는지에 따른 **결과의 책임은 사용자에게 있어요.**
- **자동 업데이트는 GitHub에서 설치 파일을 받아 실행해요.** 설치형은 기본으로 새 버전을 확인하고, 받은 설치 파일을 SHA-256으로 확인한 뒤 앱을 끝낼 때 조용히 설치해요(트레이의 "지금 업데이트하고 다시 시작"을 눌렀을 때와, 받아 둔 업데이트가 있는 채로 트레이로 자동 시작될 때도 설치해요. 자동 업데이트는 끌 수 있어요). 설치 파일에는 **코드 서명이 없어서** Windows SmartScreen 경고가 뜰 수 있어요. SHA-256 확인은 파일이 내려받는 중에 깨지거나 바뀐 것을 잡아 줄 뿐이고, 이 저장소의 계정이나 릴리스가 탈취되는 **공급망 공격은 막지 못해요.** 해시를 확인한 뒤 설치 파일을 실행하기까지의 짧은 사이에 같은 사용자 권한으로 도는 다른 프로그램이 파일을 바꾸는 것도 막지 못해요. 새 버전에 문제가 있어도 **자동으로 이전 버전으로 돌아가지 않아요.**
- **로컬 AI 요약(선택)은 제3자가 만든 엔진과 모델을 인터넷에서 내려받아요.** Ollama(MIT)와 Qwen3 8B(Apache 2.0)를 합쳐 약 6.7GB(엔진 약 1.5GB + 모델 약 5.2GB)를 받고, 끝나면 디스크를 약 7GB 차지해요. 요약하는 동안 GPU 메모리를 약 5GB 쓰고 CPU·전력도 쓰기 때문에, 같은 PC에서 게임이나 다른 무거운 프로그램이 느려질 수 있어요. 요약은 **틀리거나 빠뜨릴 수 있어요.**
- **사용량·한도·비용 표시는 추정치예요.** 실제 청구나 한도와 달라요(5조).
- **비공식 도구예요.** "Claude"는 Anthropic PBC의 상표이고, 이 프로젝트는 Anthropic과 관계가 없는 개인 프로젝트예요.

#### 3.2 사용자의 책임

다음은 **사용자의 몫**이에요: 이 PC와 Windows 계정의 보안, 운영체제와 이 소프트웨어의 업데이트, 백신·방화벽, **관제탑 세션과 받는 세션의 권한 설정과 관리**, 대화에 들어 있는 비밀 정보의 관리, 데이터 폴더(`office.config.json`·`app.log`·`dist` 등)의 접근 제한과 백업, 화면·캡처를 누구와 공유하는지의 판단, 공용·공유 PC나 믿을 수 없는 프로그램이 도는 PC에서 쓰지 않는 것, 파일을 공식 배포처에서만 받아 SHA-256을 확인하는 것.

#### 3.3 저작권자가 책임지지 않는 것

**보안사고**(예: 대화에 있던 키·토큰·비밀번호·개인정보의 노출, 무단 접근이나 무단 사용, 의도하지 않은 글의 전달과 그로 인한 작업, 뜻하지 않은 요금, 악성 프로그램·랜섬웨어 감염, 데이터의 삭제·변조·유출, 계정 정지·제재)가 다음 가운데 어느 것에서 비롯되었든, 관련 법령이 허락하는 가장 넓은 범위에서 **저작권자는 책임을 지지 않아요.**

1. 소프트웨어의 오류나 알려지지 않은 취약점(로컬 서버, 관제탑 배달, 자동 업데이트 포함)
2. 선택 구성요소(Ollama·Qwen3 등), 다른 사람이 만든 콘텐츠
3. Electron·Chromium·Node.js·Python·Windows 등 구성요소의 취약점
4. 사용자의 설정·환경·부주의(받는 세션을 `bypassPermissions`나 넓은 허용 규칙으로 둔 것, 믿을 수 없는 프로그램이 도는 PC에서 관제탑을 켠 것, 같은 PC를 여럿이 쓴 것, 대화에 비밀 정보를 둔 것 등)
5. 제3자의 공격이나 악의적 행위(같은 PC의 다른 프로그램, 업데이트 경로·저장소 계정·릴리스 파일의 변조 등)
6. Anthropic·GitHub·Ollama 등 제3자 서비스의 장애·정책 변경·보안 사고

다만 저작권자의 고의 또는 중대한 과실로 생긴 사고와 법령상 배제할 수 없는 책임은 제외해요(2조).

#### 3.4 [보내기]와 관제탑

- 관제탑 세션은 입력창의 글을 받는 세션에 **글자 그대로 전달**할 뿐이에요. 글을 받은 세션이 무엇을 하는지는 그 세션의 권한 설정과 동작에 달려 있고, 저작권자는 그 결과(데이터 손실, 파일 삭제, 의도하지 않은 외부 전송, 계정 불이익 등)에 책임지지 않아요.
- README의 "받는 세션 설정"은 Claude Code 2.1.284(Windows)에서 확인한 내용을 정리한 **참고 자료**예요. Claude Code가 바뀌면 달라질 수 있고, 그 내용이 정확하거나 안전하다고 보증하지 않아요.
- 승인·결정(설계 승인, 푸시 허용, 권한 승인 등)은 **그 세션에 직접** 입력해야 하고, 전달한 글은 승인으로 인정되지 않아요. 이 규칙을 우회하려고 글을 꾸미지 마세요.

#### 3.5 내려받는 파일(자동 업데이트·로컬 AI)

- 자동 업데이트의 설치 파일은 GitHub에서, 로컬 AI의 엔진과 모델은 GitHub와 ollama.com에서 받아요. 이 파일들이 저작권자가 아닌 곳에서 내려오는 점, 그리고 코드 서명이 없는 점을 알고 쓰세요.
- SHA-256과 크기 확인은 **위변조와 손상을 줄이는 장치일 뿐 안전을 보증하지 않아요.**
- 걱정되면 자동 업데이트를 끄고 릴리스를 직접 확인하세요. 로컬 AI를 설치하지 않아도 나머지 기능은 그대로 써요.

#### 3.6 이렇게 하시길 권해요

- 관제탑은 **전용 세션**으로 열고, 믿을 수 없는 프로그램이 도는 PC나 여러 사람이 같이 쓰는 PC에서는 켜지 마세요.
- 받는 세션에는 **좁은 허용 규칙과 `ask`·`deny` 규칙**을 두고, `bypassPermissions`는 쓰지 마세요.
- 승인·결정은 요약만 보지 말고 **원문(전문)을 확인한 뒤 그 세션에 직접** 입력하세요.
- 화면을 공유하거나 캡처하기 전에 대화 내용을 확인하세요. 대화에는 비밀 정보를 두지 마세요.
- 데이터 폴더(`%APPDATA%\ClaudeOffice`)를 남과 공유하거나 온라인에 올리지 마세요.
- 파일은 **공식 배포처에서만** 받고 SHA-256을 확인하세요.
- 사고가 의심되면: 관제탑 세션의 대기 중지 → 앱 종료(트레이 → 종료) → 받는 세션이 한 일 확인 → 노출됐을 수 있는 키·비밀번호 폐기와 재발급 → 필요하면 앱 제거와 데이터 폴더 삭제 순서로 하세요.

#### 3.7 보안 문제를 알려 주세요

취약점을 발견하면 **공개 이슈에 자세히 쓰지 말고**, 이 저장소의 **Security 탭 → "Report a vulnerability"(비공개 취약점 보고)** 로 알려 주세요([바로가기](https://github.com/BlackBuddle/ClaudeOffice-releases/security/advisories/new), [`SECURITY.md`](SECURITY.md)). 최선을 다해 살펴보지만, 처리 시점과 결과를 약속하지는 않아요.

### 4. 제3자 서비스

Anthropic의 Claude Code·Claude 데스크톱 앱·구독, GitHub, Ollama와 모델 제공처 같은 **제3자 서비스**의 약관·요금·사용 한도·중단·계정 제재·응답 오류는 그 서비스 제공자와 사용자 사이의 일이며, 저작권자는 관여하지 않고 책임지지 않아요. "Claude", "Anthropic"은 Anthropic PBC의 상표이고, 이 프로젝트는 그와 제휴·후원·승인 관계가 없는 **개인 프로젝트**예요.

### 5. 사용량·비용 표시는 참고용이에요

소프트웨어가 보여 주는 사용량·한도·비용은 대화 기록으로 계산한 **추정치**이고, 한 계정에서 맞춘 보정값으로 환산하기 때문에 계정이나 요금제에 따라 실제와 달라요. 실제 청구·한도와 다를 수 있어요. 요금과 한도의 기준은 항상 서비스 제공자가 알려 주는 값이에요.

### 6. AI가 만든 글

Claude가 만든 답과 로컬 AI가 만든 요약의 정확성·완전성·적합성은 보증하지 않아요. **요약만 보고 승인이나 결정을 하지 마세요.** "답변 대기"·"권한 대기" 표시도 대화 기록으로 추정한 것이라 틀릴 수 있어요. 의료·법률·재정·안전에 관한 중요한 결정에 쓰지 마세요.

### 7. 데이터와 백업

소프트웨어의 오류·업데이트·삭제로 설정·기록이 사라질 수 있고, [보내기]로 전달한 글이 일으킨 일 때문에 세션의 작업물이 바뀌거나 사라질 수 있어요. 중요한 것은 직접 백업하세요(버전 관리 등).

### 8. 법령상 권리

이 면책조항은 법령이 정한 소비자의 권리를 없애지 않아요. 법령이 허락하지 않는 범위에서는 이 조항의 해당 부분이 적용되지 않고, 나머지는 그대로 유효해요.

### 9. 변경과 효력

저작권자는 이 문서를 바꿀 수 있고, 새 판은 공식 배포처에 올린 때부터 그 뒤에 받거나 갱신하는 소프트웨어에 적용돼요(자동 업데이트도 갱신이에요). 소프트웨어를 설치하거나 쓰면 이 문서에 동의한 것으로 봐요.

---

## English

*A courtesy translation. If it differs from the Korean version, the Korean version prevails.*

### 1. Provided "AS IS" (no warranty)

ClaudeOffice (the "Software") is provided free of charge to personal users **"AS IS"**. To the fullest extent permitted by law, the Licensor gives no warranty of any kind, express or implied, including that it is error-free or uninterrupted, works in every environment (Windows version, display scaling, security software, other programs), is merchantable or fit for a particular purpose, does not infringe third-party rights, or that the information it shows (session status, waiting-for-answer/permission indicators, summaries, usage, limits, costs, delivery results) is accurate or complete.

### 2. Limitation of liability

To the fullest extent permitted by law, the Licensor is not liable for any **direct, indirect, special or consequential damages** (data loss, modification or deletion of files, lost profits, business interruption, account suspension or other account consequences, unexpected charges, device failure, etc.) arising from the use of, or inability to use, the Software. Because the Software is free, any liability that is found to exist is limited to the amount you paid the Licensor (zero). This does not exclude damage caused by the Licensor's **intent or gross negligence**, or liability that cannot be excluded by law (such as consumer-protection law).

### 3. Security incident disclaimer

**3.1 What the Software does.**

- (a) It **reads** the files Claude Code leaves on this PC (the running-session list, conversation records, sub-agent records, session titles and token usage under `~/.claude`, and the session files of the Claude desktop app) to show and summarize sessions. It only reads; it does not modify them. **Conversations may contain passwords, keys, personal data or confidential information, and the Software shows that content on screen as is (including the full-text view).** Secret patterns such as `sk-…`, `ghp_…` and `password=…` are masked, but **not completely**. Check before showing, capturing, recording or sharing the screen.
- (b) **Caches and records remain** in the data folder (`%APPDATA%\ClaudeOffice`): session titles, conversation excerpts, sent command texts and summaries. The folder remains after uninstalling.
- (c) The **local server has no login.** It listens only on `127.0.0.1`, so other devices cannot reach it, but **other programs on the same PC (including malware) and other Windows user accounts on the same PC** may read the session list and full conversation text or put text into the command queue. Requests with an unfamiliar Host name, and command / full-text / summary requests coming from other websites, are rejected; this does not stop programs on the same PC.
- (d) **Text sent with [Send] can cause real work.** When the control-tower session relays text to another Claude session, depending on that session's permission settings, real actions — **editing or deleting files, running commands, sending data out** — may follow. Relayed text is treated as a request from another session, not as your approval; but if the receiving session is configured to work without asking (allow rules, auto mode, `bypassPermissions`, etc.), work may proceed while you are not watching. **You are responsible for the consequences** of what you send and how you configure the receiving session.
- (e) **Automatic update downloads an installer from GitHub and runs it.** The installed edition checks for new versions by default, verifies the downloaded installer with SHA-256 and installs it silently when the app exits (also when you choose "update and restart" in the tray menu, and when the app auto-starts into the tray with a downloaded update waiting; automatic update can be turned off). The installer has **no code signature**, so Windows SmartScreen may warn. SHA-256 verification only catches corruption or alteration during download; it **does not prevent supply-chain attacks** in which this repository's account or releases are compromised, nor another program running with the same user rights replacing the file in the short gap between the hash check and running it. If a new version is faulty, the app **does not roll back** to the previous version automatically.
- (f) **The optional local AI summary downloads third-party engine and model files from the internet** — Ollama (MIT) and Qwen3 8B (Apache 2.0), about 6.7 GB in total (engine about 1.5 GB + model about 5.2 GB), occupying about 7 GB of disk afterwards. While summarizing it uses about 5 GB of GPU memory plus CPU and power, which may slow games or other heavy programs on the same PC. Summaries **may be wrong or incomplete.**
- (g) **Usage, limit and cost figures are estimates** and differ from actual billing or limits (Section 5).
- (h) **This is an unofficial tool.** "Claude" is a trademark of Anthropic PBC; this is a personal project unrelated to Anthropic.

**3.2 Your responsibility.** Security of your PC and Windows account, updates of the OS and the Software, antivirus and firewall, **the permission settings and management of the control-tower session and the receiving sessions**, managing secrets that appear in conversations, access control and backup of the data folder, deciding whom you share the screen or captures with, not using the Software on shared PCs or PCs running untrusted programs, and downloading only from the Official Distribution and verifying SHA-256.

**3.3 What the Licensor is not responsible for.** To the fullest extent permitted by law, the Licensor is not responsible for any security incident (exposure of keys, tokens, passwords or personal data found in conversations; unauthorized access or use; relaying of unintended text and the work that follows; unexpected charges; malware or ransomware; deletion, tampering or leakage of data; account suspension or sanctions) regardless of whether it arises from (1) errors or unknown vulnerabilities in the Software, including the local server, control-tower delivery and automatic update, (2) Optional Components (Ollama, Qwen3, etc.) or other people's content, (3) vulnerabilities in components such as Electron, Chromium, Node.js, Python or Windows, (4) your settings, environment or carelessness (leaving a receiving session on `bypassPermissions` or broad allow rules, running the control tower on a PC with untrusted programs, sharing the PC, keeping secrets in conversations, etc.), (5) attacks by third parties (other programs on the same PC, tampering with the update path, repository account or release files, etc.), or (6) outages, policy changes or security incidents of third-party services such as Anthropic, GitHub or Ollama. Incidents caused by the Licensor's intent or gross negligence, and liability that cannot be excluded by law, are not excluded.

**3.4 [Send] and the control tower.** The control-tower session only relays your text to the receiving session verbatim. What the receiving session then does depends on its permission settings and behavior, and the Licensor is not responsible for the result (data loss, deleted files, unintended outbound transfers, account consequences, etc.). The "receiving-session settings" in the README are a **reference** compiled from Claude Code 2.1.284 on Windows; they may change as Claude Code changes and are not guaranteed to be accurate or safe. Approvals and decisions (design approval, push permission, permission prompts, etc.) must be entered **directly in that session**; relayed text is not accepted as approval. Do not disguise text to get around this rule.

**3.5 Downloaded files (automatic update and local AI).** Update installers come from GitHub; the local AI engine and model come from GitHub and ollama.com — not from the Licensor — and the installer has no code signature. SHA-256 and size checks only reduce tampering and corruption; **they do not guarantee safety.** If this worries you, turn automatic update off and check releases yourself. The rest of the Software works without the local AI.

**3.6 Recommendations.** Use a **dedicated session** as the control tower and do not run it on PCs with untrusted programs or shared PCs. Give receiving sessions **narrow allow rules plus `ask`/`deny` rules** and do not use `bypassPermissions`. For approvals and decisions, **read the original text, not just a summary, and enter them directly in that session.** Check conversation content before sharing or capturing the screen, and keep secrets out of conversations. Do not share or upload the data folder. Download only from the **Official Distribution** and verify SHA-256. If you suspect an incident: stop the control-tower session's wait → quit the app (tray → Exit) → review what the receiving sessions did → revoke and reissue any exposed keys or passwords → if needed, uninstall and delete the data folder.

**3.7 Reporting a security problem.** Do not post vulnerability details in a public issue. Use the **Security tab → "Report a vulnerability"** (private vulnerability reporting) of this repository ([report here](https://github.com/BlackBuddle/ClaudeOffice-releases/security/advisories/new); see also `SECURITY.md`). The Licensor will do his best but does not promise a response time or outcome.

### 4. Third-party services

Terms, prices, usage limits, outages, account sanctions and response errors of third-party services such as Anthropic's Claude Code, Claude desktop app and subscriptions, GitHub, and Ollama and model providers are matters between you and the service provider; the Licensor is not involved and not responsible. "Claude" and "Anthropic" are trademarks of Anthropic PBC; this is a personal project not affiliated with, sponsored by or approved by Anthropic.

### 5. Usage and cost figures are for reference only

They are **estimates** computed from conversation records and converted with a calibration value fitted on one account, so they differ by account and plan, and may differ from actual billing or limits. The service provider's figures are always authoritative.

### 6. AI-generated text

The accuracy, completeness and suitability of Claude's answers and of local-AI summaries are not guaranteed. **Do not approve or decide based on a summary alone.** The "waiting for answer" and "waiting for permission" indicators are estimated from conversation records and can be wrong. Do not rely on them for important medical, legal, financial or safety decisions.

### 7. Data and backups

Settings and records may be lost due to bugs, updates or deletion, and text relayed with [Send] may change or destroy a session's work. Back up what matters (version control, etc.).

### 8. Statutory rights

This disclaimer does not remove consumer rights granted by law. To the extent a part is not permitted by law it does not apply, and the rest remains in force.

### 9. Changes and effect

The Licensor may change this document; a new version applies from the time it is posted to the Official Distribution to Software received or updated after that time (automatic updates count as updates). Installing or using the Software means you accept this document.
