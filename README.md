# 결재 문서 작성 도우미

업무 보고, 기안, 협조, 지출, 채용·근태 등 결재 문서 초안을 위한 한국어 가이드입니다. Claude용 플러그인 버전은 1.0.0입니다. 가이드에 나오는 화면과 값은 작성 방법을 보여 주는 예시입니다. 실제 서식의 항목·필수 조건·결재선을 기준으로 작성하세요.

## 가이드로 바로 작성하기

1. 목적에 맞는 가이드를 고르고 준비할 자료, 입력 순서, 가상 예시를 확인합니다. [업무 보고 작성 가이드](docs/forms/work-report.md) · [다른 결재 서식 목록](plugins/approval-writing/skills/approval-forms/references/guide-index.md)
2. 직접 작성하거나, AI에 초안을 요청할 때는 해당 가이드의 요청문을 복사하거나 Markdown 파일을 첨부합니다. 이미 알고 있는 화면 항목명과 업무 메모를 함께 제공합니다.
3. 초안의 입력값을 실제 화면에 옮깁니다. HTML 본문을 받았고 화면에 HTML 탭이 있으면 코드만 붙여 넣고 Editor에서 글꼴·표·줄바꿈을 확인합니다. 제출 전 첨부·연관문서·결재선을 직접 확인합니다.

본문의 기본 글꼴은 Sans Serif입니다. HTML에서는 바깥 `div`에 `font-family:sans-serif`를 지정합니다. [공통 디자인 기준](plugins/approval-writing/skills/work-report/references/design.md)

> 첨부한 채용 요청서 작성 가이드를 읽고, 가상 출고팀 포장 담당 정규직 1명을 모집하는 요청서를 작성해 주세요. 공고 희망 기간은 11월 16~27일입니다. 화면에 옮길 값, 세부 내용, 제출 전 확인사항을 주세요.

## 플러그인 설치하기

### Codex

이 공개 저장소의 일반형 `approval-writing` 플러그인은 Codex 배포를 종료했습니다. 이 안내의 적용 범위는 이 저장소의 일반형 플러그인입니다. 조직에서 별도로 제공하는 전용 플러그인을 사용하는 경우 해당 조직의 설치·업데이트 안내를 따릅니다.

공개 가이드만 사용하는 경우에는 위 작성 가이드의 요청문을 복사하거나 가이드 Markdown 파일을 대화에 첨부할 수 있습니다. 이미 전용 플러그인이 설치된 환경에서는 설치된 스킬과 동봉 가이드를 먼저 확인하고, 사용자가 해당 문서에 지정한 서식을 우선합니다.

### Claude Code

저장소를 복제하거나 압축을 푼 뒤, 이 README가 있는 최상위 폴더에서 다음 명령을 실행합니다.

```text
/plugin marketplace add .
/plugin install approval-writing@approval-writing-guides
```

### Claude Cowork

Git에 배포된 버전은 **Customize → Plugins → Add marketplace**에서 저장소 주소를 등록한 뒤 **결재 문서 작성 도우미**를 설치합니다. 조직에서 플러그인을 관리한다면 해당 조직의 설치 안내를 확인합니다. [Claude Cowork 플러그인 안내](https://claude.com/docs/cowork/guide/plugins)

## 설치 후 사용하기

| 하려는 일 | Claude에서 사용할 스킬 |
|---|---|
| 진행 상황과 업무 결과 공유 | `$work-report` |
| 결재 서식 선택과 초안 작성 | `$approval-forms` |

Claude에서는 스킬 이름과 요청을 문장으로 입력해도 됩니다. 결재 서식을 이미 골랐다면 새 대화에서 서식명과 업무 메모를 함께 알려 주세요.

> $approval-forms 채용 요청서로 작성해 주세요. 가상 출고팀에 포장 담당 정규직 1명이 필요합니다. 공고 희망 기간은 11월 16~27일입니다. 화면 입력값, 세부 내용, 작성자 확인사항을 주세요.

서식이 불명확하면 누가 무엇을 판단하거나 해야 하는지부터 적습니다. 업무 보고는 진행·결과와 이번 판단 요청을 구분합니다. [업무 보고 스킬](plugins/approval-writing/skills/work-report/SKILL.md) · [결재 서식 작성 스킬](plugins/approval-writing/skills/approval-forms/SKILL.md)
