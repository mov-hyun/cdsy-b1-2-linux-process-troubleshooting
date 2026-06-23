# cdsy-b1-2-linux-process-troubleshooting

`agent-leak-app`을 Linux 환경에서 실행하며 관찰한 프로세스 장애 상황과 트러블슈팅 과정을 정리하는 저장소입니다.

## Overview

이 저장소에는 실험에 사용한 스크립트, 수집한 관제 자료, 그리고 장애 분석 리포트를 순서대로 정리합니다. 실행 환경은 이전 단계에서 구성한 Linux 실습 환경을 이어서 사용합니다.

## Environment

- Linux 실습 환경: OrbStack
- 실행 계정: `agent-admin`
- 대상 앱: `agent-leak-app`
- 앱 포트: `15034`
- 작업 경로: `/home/agent-admin/b1-2-agent-leak`

제공 실행 파일과 로컬 환경에서 생성되는 로그, 키 파일, 임시 파일은 저장소에 포함하지 않습니다.

## Structure

```text
.
├── scripts/
├── evidence/
├── reports/
└── README.md
```

## Scripts

```text
scripts/
├── setup_agent_home.sh
├── run_agent.sh
└── monitor.sh
```

실험 환경 준비, 앱 실행, 상태 관찰에 필요한 스크립트를 이곳에 둡니다.

## Evidence

```text
evidence/
├── oom/
│   ├── before/
│   └── after/
├── cpu/
│   ├── before/
│   └── after/
└── deadlock/
    ├── before/
    └── after/
```

실험 중 확인한 로그, 명령어 출력, 관제 결과를 상황별로 나누어 보관합니다.

## Reports

```text
reports/
├── 01-oom-crash.md
├── 02-cpu-spike.md
└── 03-deadlock.md
```

수집한 증거를 바탕으로 장애별 분석 내용을 정리합니다.

## Notes

- 로컬에서 생성되는 실행 파일, 로그, 키 파일은 `.gitignore`로 제외합니다.
- 분석 내용은 실제 실행 결과가 쌓인 뒤 단계적으로 보완합니다.
