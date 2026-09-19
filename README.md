# 웹툰공방 — 배포 안내

이 저장소는 **설치 파일과 안내문만** 둡니다. 소스 코드는 비공개입니다.
설치 파일은 오른쪽 **Releases**에서 받습니다.

## 받을 파일

| 장비 | 파일 |
|---|---|
| 윈도우 10/11 (x64) | `webtoon-gongbang-<버전>-win-x64.exe` |
| 맥 (Apple Silicon) | `webtoon-gongbang-<버전>-mac-arm64.dmg` |

ARM 윈도우는 x64 설치 파일이 에뮬레이션으로 실행됩니다(변환 속도는 느립니다). 인텔 맥은 지원하지 않습니다.

## 설치

- **윈도우**: exe를 실행합니다. 설치 폴더를 고를 수 있습니다. SmartScreen 경고가 뜨면 "추가 정보 → 실행"을 누릅니다(서명 인증서 없음).
- **맥**: dmg를 열고 앱을 응용 프로그램 폴더로 끌어 놓습니다. 처음 한 번은 **우클릭 → 열기**로 실행합니다(공증 없음).

## 여는 파일

- `.skp` 스케치업 파일. 구버전 파일은 스케치업에서 최신 버전으로 다시 저장한 뒤 엽니다.
- `.wtg` 웹툰공방 파일. 변환된 모델과 장면·카메라·광원·선 설정을 담고 있어 다시 변환하지 않고 바로 열립니다. 저장하면 SKP가 있던 폴더에 같은 이름으로 만들어집니다.

## 문제 신고

앱의 정보 창에서 "GitHub 이슈로 보내기"를 누르거나, 이 저장소의 Issues에 남깁니다.
메일: lion38826977@gmail.com

## 라이선스 고지

웹툰공방은 비공개 소프트웨어입니다. 아래 오픈소스 구성요소를 포함하며, 각 라이선스 원문은 설치 폴더 안(`resources/vendor`, `resources/python`, Electron의 `LICENSE.electron.txt`·`LICENSES.chromium.html`)에 그대로 들어 있습니다.

| 구성요소 | 라이선스 |
|---|---|
| OpenSKP 1.2.0 (SKP 읽기) | MIT |
| shapely 2.1.2 | BSD-3-Clause |
| GEOS (shapely가 쓰는 기하 엔진, 별도 DLL로 동적 링크) | LGPL-2.1 |
| trimesh 5.1.0 | MIT |
| defusedxml 0.7.1 | PSF-2.0 |
| NumPy 2.3.5 (OpenBLAS 포함) | BSD-3-Clause |
| Pillow 12.3.0 | MIT-CMU |
| Python 3.12 (python-build-standalone) | PSF-2.0 |
| Electron 38 / Chromium | MIT / BSD-3-Clause |
| ffmpeg (Chromium 동봉, 별도 DLL로 동적 링크) | LGPL-2.1 |
| Microsoft Visual C++ 런타임 | Microsoft 재배포 조건 |

LGPL 구성요소(GEOS, ffmpeg)는 별도 라이브러리 파일로 배포되므로 같은 이름의 파일로 교체할 수 있습니다. 소스는 각 프로젝트(https://libgeos.org, https://ffmpeg.org)에서 받을 수 있습니다.
