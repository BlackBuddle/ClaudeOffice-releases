# ClaudeOffice — 제3자 구성 요소 고지 (Third-Party Notices)

ClaudeOffice 설치 파일(`ClaudeOffice-Setup-<버전>.exe`)과 휴대용 실행 파일(`ClaudeOffice-Portable-<버전>.exe`)에는 아래의 제3자 구성 요소가 들어 있습니다. 각 구성 요소는 그 저작권자의 것이며, 아래 적은 라이선스에 따라 함께 배포합니다. ClaudeOffice 자체의 사용 조건은 [LICENSE](LICENSE) 파일에 있고, 그 조건은 이 구성 요소들의 라이선스가 주는 권리를 제한하지 않습니다.

기준: v1.0.0(2026-10-01 빌드)과 v1.0.1(2026-10-02 빌드) 설치 파일 — 두 버전의 구성 요소는 같아요. 구성 요소가 바뀌면 이 파일도 함께 고칩니다. 이 목록에서 빠진 것이나 틀린 것을 발견하면 [Issues](https://github.com/BlackBuddle/ClaudeOffice-releases/issues)로 알려 주세요.

이 파일은 설치 폴더에 들어 있는 고지 파일과 각 프로젝트의 공식 배포 조건을 읽어 정리했습니다.

## A. 설치 파일과 휴대용 파일에 들어 있는 것

### A-1. Electron 44.4.5

- 라이선스: MIT License (부록 1)
- Copyright (c) Electron contributors, Copyright (c) 2013-2020 GitHub Inc.
- 설치 폴더의 `LICENSE.electron.txt`에도 같은 문구가 들어 있습니다.
- 소스: https://github.com/electron/electron

### A-2. Chromium 152.0.7977.130 및 Electron에 내장된 구성 요소

Electron 안에는 다음이 들어 있고, 각각의 저작권 표시와 라이선스 전문은 설치 폴더의 **`LICENSES.chromium.html`**(약 20MB)에 있습니다. 분량이 커서 이 파일에 옮기지 않았습니다.

- Chromium과 그 하위 구성 요소 — V8(15.2.124.28-electron.0), Skia, BoringSSL, Brotli, FreeType, libjpeg-turbo, SQLite, zlib, WebRTC, SwiftShader, Vulkan 로더 구성 요소, DirectX Shader Compiler 등
- **Node.js 24.21.0** — MIT License (Electron에 내장)
- **FFmpeg** — 설치 폴더의 `ffmpeg.dll`은 별도 파일로 들어 있습니다. FFmpeg의 대부분은 GNU Lesser General Public License v2.1 이상(LGPL v2.1+)이고, 일부 파일은 MIT·BSD 계열입니다. 고치지 않은 Electron 배포본 그대로입니다. 소스: https://git.ffmpeg.org/ffmpeg.git , 필요하면 Issues로 요청하세요.
- **Microsoft Direct3D 구성 요소** — `d3dcompiler_47.dll`은 파일 정보에 "Direct3D HLSL Compiler for Redistribution"(Microsoft Corporation)으로 적힌, Microsoft가 재배포용으로 제공하는 Windows 구성 요소입니다. 재배포 조건은 Microsoft가 이 구성 요소에 정한 조건을 따릅니다. `dxcompiler.dll`·`dxil.dll`(DirectX Shader Compiler)의 고지는 `LICENSES.chromium.html`에 있습니다.

### A-3. Python 3.14.7 (수집기를 돌리는 개인 사본)

설치 폴더의 `resources\office\python`에 Python 표준 구성(tkinter와 시험 코드는 뺌)이 들어 있습니다. 사용자 PC에 Python을 설치하거나 PATH를 바꾸지 않으며, 수집기만 이 사본으로 실행합니다.

- 라이선스: Python Software Foundation License Version 2 (부록 2). 그 2항에 따라 "Copyright (c) 2001 Python Software Foundation; All Rights Reserved" 표시와 라이선스를 부록 2에 그대로 두었습니다.
- Python 배포본의 전체 고지(역사, BeOpen·CNRI·CWI 라이선스, 아래 일부 구성 요소의 고지)는 설치 폴더의 **`resources\office\python\LICENSE.txt`**에 있습니다. 이 파일에 옮기지 않았습니다.
- 이 Python 사본에 딸린 구성 요소 (`DLLs` 폴더 등)

  | 구성 요소 | 파일 | 라이선스 | 근거 |
  |---|---|---|---|
  | OpenSSL 3.5.7 | `libssl-3.dll`, `libcrypto-3.dll` | Apache License 2.0 | `python\LICENSE.txt`(Apache 2.0 전문 수록), Python 공식 문서(OpenSSL 3.0 이후는 Apache License 2.0) |
  | bzip2 1.0.8 (Julian Seward) | `_bz2.pyd` | bzip2 라이선스(BSD 계열) | `python\LICENSE.txt` |
  | libffi (Anthony Green, Red Hat 외) | `libffi-8.dll` | MIT 계열 | `python\LICENSE.txt` |
  | Zstandard (Meta Platforms) | `_zstd.pyd` | BSD 라이선스 | `python\LICENSE.txt` |
  | Microsoft Visual C++ 런타임 | `vcruntime140.dll`, `vcruntime140_1.dll` | Microsoft Distributable Code (재배포 조건은 Python 배포본이 적은 "Additional Conditions for this Windows binary build"를 따릅니다) | `python\LICENSE.txt` |
  | SQLite 3.50.4 | `sqlite3.dll`, `_sqlite3.pyd` | 공개 도메인 | SQLite 공식 저장소의 LICENSE.md ("SQLite Is Public Domain") |
  | zlib 계열(zlib, zlib-ng) | `zlib1.dll` | zlib 라이선스 | DLL 파일 정보(zlib, Copyright (C) 1995-2026 Jean-loup Gailly & Mark Adler), zlib-ng 공식 저장소의 LICENSE.md |
  | Expat | `pyexpat.pyd` | MIT License | Python 공식 문서(expat 절), libexpat 공식 저장소의 COPYING |
  | libmpdec (Stefan Krah) | `_decimal.pyd` | BSD 2-Clause License | Python 공식 문서(libmpdec 절: "Copyright (c) 2008-2024 Stefan Krah") |
  | XZ Utils (liblzma) | `_lzma.pyd` | BSD Zero Clause License (0BSD) | XZ Utils 공식 저장소의 COPYING ("liblzma is under the BSD Zero Clause License") |
  | libtommath | `libtommath.dll` | Unlicense (공개 도메인 헌정) | libtommath 공식 저장소의 LICENSE ("The LibTom license") |

  `python\LICENSE.txt`에는 사용하지 않는 Tcl/Tk 고지도 남아 있습니다(tkinter를 뺐으므로 Tcl/Tk는 들어 있지 않습니다). 위 구성 요소의 정확한 배포 조건은 해당 프로젝트의 공식 배포 조건을 따릅니다.

### A-4. NSIS 3.0.4.1 (설치 프로그램의 제작 도구)

`ClaudeOffice-Setup-<버전>.exe`와 휴대용 실행 파일을 만드는 데 쓴 Nullsoft Scriptable Install System의 실행 코드(설치 프로그램 stub와 압축 해제 코드)가 그 파일 안에 들어 있습니다.

- Copyright (C) 1999-2018 Contributors
- NSIS의 소스 코드·플러그인·문서·예제·헤더·그림은 **zlib/libpng 라이선스**(부록 3)이고, zlib 압축 모듈도 zlib/libpng 라이선스입니다. bzip2 압축 모듈은 bzip2 라이선스, **LZMA 압축 모듈은 Common Public License 1.0**입니다.
- LZMA 모듈에는 특별 예외가 있습니다. LZMA 모듈의 저자(Igor Pavlov, Amir Szekely)는 LZMA 모듈의 파일에 코드를 정적·동적으로 연결하는 것을 허락하며, 그렇게 연결한 코드는 Common Public License의 적용을 받지 않습니다. LZMA 모듈 파일 자체를 고치거나 더한 부분에는 Common Public License가 적용됩니다. ClaudeOffice는 NSIS 자체의 파일을 고치지 않고 설치 스크립트(안내 화면의 옵션)만 따로 작성했습니다.
- 각 라이선스 전문은 NSIS 배포본의 `COPYING` 파일에 있습니다(https://nsis.sourceforge.io). 제작에 쓴 빌드 도구(electron-builder 26.15.3, MIT License)의 코드는 설치 파일에 들어 있지 않습니다.

### A-5. elevate.exe

설치 폴더의 `resources\elevate.exe`는 설치 프로그램 제작 도구(electron-builder)의 NSIS 구성 요소에 딸려 들어오는 Windows용 권한 상승 도우미입니다. 파일 정보상 이름은 "Elevate", 제작자는 Johannes Passing, "Copyright (C) 2007"입니다. 이 프로그램의 공식 저장소(https://github.com/jpassing/elevate)는 MIT License로 공개돼 있고, 이 파일의 라이선스는 해당 프로젝트의 공식 배포 조건을 따릅니다.

### A-6. 번들 글꼴 (Silkscreen, VT323)

화면의 도트 글씨(이름표·숫자·표시판)에 쓰는 글꼴 두 가지가 앱에 들어 있습니다. 인터넷에서 받지 않습니다.

| 글꼴 | 파일 | 저작권 | 라이선스 |
|---|---|---|---|
| Silkscreen (보통·굵게) | `Silkscreen-Regular.ttf`, `Silkscreen-Bold.ttf` | Copyright 2001 The Silkscreen Project Authors (https://github.com/googlefonts/silkscreen) | SIL Open Font License 1.1 (부록 4) |
| VT323 | `VT323-Regular.ttf` | Copyright 2011, The VT323 Project Authors | SIL Open Font License 1.1 (부록 4) |

- 글꼴 파일과 각 글꼴의 라이선스 원문(`OFL-Silkscreen.txt`, `OFL-VT323.txt`)이 설치 폴더의 `resources\office\dist\fonts\`에 함께 들어 있습니다.
- 한글 본문은 사용자 PC의 Windows 기본 글꼴(맑은 고딕)을 씁니다. 이 글꼴 파일은 ClaudeOffice에 들어 있지 않습니다.

## B. 선택해서 내려받는 구성 요소 (설치 파일에 들어 있지 않음)

로컬 AI 요약을 설치할 때 앱이 아래를 인터넷에서 내려받습니다. 이것들은 ClaudeOffice의 일부가 아니며, 내려받을 때 각자의 라이선스를 따릅니다. 이미 PC에 Ollama나 모델이 있으면 그것을 쓰고 없는 것만 받습니다.

### B-1. Ollama v0.35.0

- 출처: https://github.com/ollama/ollama (릴리스 `ollama-windows-amd64.zip`)
- 라이선스: MIT License — Copyright (c) Ollama (부록 1)
- 이 배포 zip에는 llama.cpp 등 하위 구성 요소와 NVIDIA CUDA 런타임 같은 제3자 파일이 들어 있고, 각각의 고지는 내려받은 폴더의 `lib\ollama` 안 LICENSE 파일들에 있습니다. 이 구성은 Ollama 배포본의 것이며 ClaudeOffice가 정한 것이 아닙니다.

### B-2. Qwen3 8B (`qwen3:8b`)

- 출처: https://ollama.com/library/qwen3 (Qwen 팀, Alibaba Cloud)
- 라이선스: Apache License 2.0 (https://www.apache.org/licenses/LICENSE-2.0)

## C. 함께 쓰지만 이 소프트웨어에 들어 있지 않은 것

- **Claude Code**와 **Claude 데스크톱 앱**은 Anthropic PBC의 제품이며 ClaudeOffice에 들어 있지 않습니다. ClaudeOffice는 이 프로그램들이 PC에 남긴 파일을 읽고, Claude 앱의 세션 사이 메시지 기능을 이용할 뿐이며, 각 제품은 Anthropic의 약관을 따릅니다. "Claude"와 "Anthropic"은 Anthropic PBC의 상표이고, ClaudeOffice는 Anthropic과 관계가 없는 개인 프로젝트입니다.

---

## 부록 1. MIT License

적용: Electron(A-1), Node.js(A-2), Ollama(B-1). 아래 문구는 설치 폴더의 `LICENSE.electron.txt`와 같고, 구성 요소마다 저작권 표시가 다릅니다(위 각 항목에 적었습니다).

```
Copyright (c) Electron contributors
Copyright (c) 2013-2020 GitHub Inc.

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```

## 부록 2. Python Software Foundation License Version 2

적용: Python 3.14.7(A-3). Python 배포본의 `LICENSE.txt`에서 그대로 옮겼습니다.

```
PYTHON SOFTWARE FOUNDATION LICENSE VERSION 2
--------------------------------------------

1. This LICENSE AGREEMENT is between the Python Software Foundation
("PSF"), and the Individual or Organization ("Licensee") accessing and
otherwise using this software ("Python") in source or binary form and
its associated documentation.

2. Subject to the terms and conditions of this License Agreement, PSF hereby
grants Licensee a nonexclusive, royalty-free, world-wide license to reproduce,
analyze, test, perform and/or display publicly, prepare derivative works,
distribute, and otherwise use Python alone or in any derivative version,
provided, however, that PSF's License Agreement and PSF's notice of copyright,
i.e., "Copyright (c) 2001 Python Software Foundation; All Rights Reserved"
are retained in Python alone or in any derivative version prepared by Licensee.

3. In the event Licensee prepares a derivative work that is based on
or incorporates Python or any part thereof, and wants to make
the derivative work available to others as provided herein, then
Licensee hereby agrees to include in any such work a brief summary of
the changes made to Python.

4. PSF is making Python available to Licensee on an "AS IS"
basis.  PSF MAKES NO REPRESENTATIONS OR WARRANTIES, EXPRESS OR
IMPLIED.  BY WAY OF EXAMPLE, BUT NOT LIMITATION, PSF MAKES NO AND
DISCLAIMS ANY REPRESENTATION OR WARRANTY OF MERCHANTABILITY OR FITNESS
FOR ANY PARTICULAR PURPOSE OR THAT THE USE OF PYTHON WILL NOT
INFRINGE ANY THIRD PARTY RIGHTS.

5. PSF SHALL NOT BE LIABLE TO LICENSEE OR ANY OTHER USERS OF PYTHON
FOR ANY INCIDENTAL, SPECIAL, OR CONSEQUENTIAL DAMAGES OR LOSS AS
A RESULT OF MODIFYING, DISTRIBUTING, OR OTHERWISE USING PYTHON,
OR ANY DERIVATIVE THEREOF, EVEN IF ADVISED OF THE POSSIBILITY THEREOF.

6. This License Agreement will automatically terminate upon a material
breach of its terms and conditions.

7. Nothing in this License Agreement shall be deemed to create any
relationship of agency, partnership, or joint venture between PSF and
Licensee.  This License Agreement does not grant permission to use PSF
trademarks or trade name in a trademark sense to endorse or promote
products or services of Licensee, or any third party.

8. By copying, installing or otherwise using Python, Licensee
agrees to be bound by the terms and conditions of this License
Agreement.
```

## 부록 3. zlib/libpng License

적용: NSIS 3.0.4.1(A-4). NSIS 배포본의 `COPYING`에서 그대로 옮겼습니다.

```
Copyright (C) 1999-2018 Contributors

This software is provided 'as-is', without any express or implied warranty. In no event will the authors be held liable for any damages arising from the use of this software.

Permission is granted to anyone to use this software for any purpose, including commercial applications, and to alter it and redistribute it freely, subject to the following restrictions:

      1. The origin of this software must not be misrepresented; you must not claim that you wrote the original software. If you use this software in a product, an acknowledgment in the product documentation would be appreciated but is not required.

      2. Altered source versions must be plainly marked as such, and must not be misrepresented as being the original software.

      3. This notice may not be removed or altered from any source distribution.
```

## 부록 4. SIL Open Font License, Version 1.1

적용: Silkscreen, VT323(A-6). 두 글꼴의 라이선스 문구는 같고, 글꼴마다 저작권 표시가 다릅니다(A-6 표에 적었습니다). 각 글꼴의 원문은 설치 폴더의 `OFL-Silkscreen.txt`·`OFL-VT323.txt`에 있습니다(VT323 원문의 저작권 줄에는 저작권자의 연락처가 함께 적혀 있어, 이 파일에는 저작권자 이름까지만 적었습니다).

```
This Font Software is licensed under the SIL Open Font License, Version 1.1.
This license is copied below, and is also available with a FAQ at:
https://scripts.sil.org/OFL


-----------------------------------------------------------
SIL OPEN FONT LICENSE Version 1.1 - 26 February 2007
-----------------------------------------------------------

PREAMBLE
The goals of the Open Font License (OFL) are to stimulate worldwide
development of collaborative font projects, to support the font creation
efforts of academic and linguistic communities, and to provide a free and
open framework in which fonts may be shared and improved in partnership
with others.

The OFL allows the licensed fonts to be used, studied, modified and
redistributed freely as long as they are not sold by themselves. The
fonts, including any derivative works, can be bundled, embedded, 
redistributed and/or sold with any software provided that any reserved
names are not used by derivative works. The fonts and derivatives,
however, cannot be released under any other type of license. The
requirement for fonts to remain under this license does not apply
to any document created using the fonts or their derivatives.

DEFINITIONS
"Font Software" refers to the set of files released by the Copyright
Holder(s) under this license and clearly marked as such. This may
include source files, build scripts and documentation.

"Reserved Font Name" refers to any names specified as such after the
copyright statement(s).

"Original Version" refers to the collection of Font Software components as
distributed by the Copyright Holder(s).

"Modified Version" refers to any derivative made by adding to, deleting,
or substituting -- in part or in whole -- any of the components of the
Original Version, by changing formats or by porting the Font Software to a
new environment.

"Author" refers to any designer, engineer, programmer, technical
writer or other person who contributed to the Font Software.

PERMISSION & CONDITIONS
Permission is hereby granted, free of charge, to any person obtaining
a copy of the Font Software, to use, study, copy, merge, embed, modify,
redistribute, and sell modified and unmodified copies of the Font
Software, subject to the following conditions:

1) Neither the Font Software nor any of its individual components,
in Original or Modified Versions, may be sold by itself.

2) Original or Modified Versions of the Font Software may be bundled,
redistributed and/or sold with any software, provided that each copy
contains the above copyright notice and this license. These can be
included either as stand-alone text files, human-readable headers or
in the appropriate machine-readable metadata fields within text or
binary files as long as those fields can be easily viewed by the user.

3) No Modified Version of the Font Software may use the Reserved Font
Name(s) unless explicit written permission is granted by the corresponding
Copyright Holder. This restriction only applies to the primary font name as
presented to the users.

4) The name(s) of the Copyright Holder(s) or the Author(s) of the Font
Software shall not be used to promote, endorse or advertise any
Modified Version, except to acknowledge the contribution(s) of the
Copyright Holder(s) and the Author(s) or with their explicit written
permission.

5) The Font Software, modified or unmodified, in part or in whole,
must be distributed entirely under this license, and must not be
distributed under any other license. The requirement for fonts to
remain under this license does not apply to any document created
using the Font Software.

TERMINATION
This license becomes null and void if any of the above conditions are
not met.

DISCLAIMER
THE FONT SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO ANY WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT
OF COPYRIGHT, PATENT, TRADEMARK, OR OTHER RIGHT. IN NO EVENT SHALL THE
COPYRIGHT HOLDER BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
INCLUDING ANY GENERAL, SPECIAL, INDIRECT, INCIDENTAL, OR CONSEQUENTIAL
DAMAGES, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF THE USE OR INABILITY TO USE THE FONT SOFTWARE OR FROM
OTHER DEALINGS IN THE FONT SOFTWARE.
```
