---
layout: post
title: "박사과정 연구 데이터베이스로 Obsidian 활용하기 (3) - PhD dashboard"
date: 2026-04-07 10:30:00 +0900
description: "Obsidian의 최상위 운영 화면인 PhD Dashboard를 어떻게 정리했고, Active Projects, Today's Todo, Publications, Reading Queue를 어떤 기준으로 설계했는지 정리합니다."
tags: [obsidian, research, phd, dashboard, productivity, medical-ai]
---

이 글은 박사과정 연구를 위한 Obsidian 시스템을 정리하는 시리즈의 3편이다. 1편에서는 전체 구조와 설계 원칙을 정리했고, 2편에서는 공용 논문 데이터베이스와 `Literature Dashboard`를 다뤘다. 이번 글에서는 그 위에 올라가는 최상위 운영 화면인 `PhD Dashboard`를 정리해보려 한다.

- 1편: [전체 overview]({% post_url 2026-04-04-obsidian-for-phd-research %})
- 2편: [literature dashboard]({% post_url 2026-04-06-obsidian-for-phd-research-literature-dashboard %})
- 3편: PhD dashboard

내가 원했던 것은 예쁜 홈 화면이 아니라, 박사과정 연구의 현재 상태를 매일 빠르게 복원할 수 있는 조종석이었다. 여러 프로젝트를 동시에 움직이고, 읽어야 할 논문과 이미 낸 실적을 같이 관리하다 보면 정보의 양보다 전환 비용이 더 큰 문제가 된다. 오늘 어디서 시작해야 하는지, 지금 밀려 있는 읽기 큐가 무엇인지, 내 실적이 어디에 쌓이고 있는지를 한 화면에서 바로 확인할 수 있어야 했다.

## 왜 별도의 PhD Dashboard가 필요한가

문헌 전용 대시보드만으로는 일상적인 연구 운영이 완성되지 않는다. 실제 박사과정의 하루는 다음 질문들로 시작된다.

- 지금 활성 프로젝트는 무엇인가
- 오늘 바로 처리해야 할 작업은 무엇인가
- 내가 지금까지 낸 성과는 어디에 정리되어 있는가
- 읽어야 할 논문 큐는 어느 정도 쌓여 있는가

이 네 가지가 서로 다른 노트와 폴더에 흩어져 있으면, 구조는 있어도 실행 속도는 느려진다. 그래서 `PhD Dashboard`는 단순한 링크 모음이 아니라, 프로젝트 실행, 일일 작업, 실적 기록, 문헌 큐를 하나의 운영 화면으로 묶는 역할을 맡는다.

## 이번에 PhD Dashboard에서 정리한 기준

이번 작업에서는 상위 화면을 더 늘리지 않고, 가장 필요한 네 섹션만 남기기로 했다.

1. `Active Projects`
2. `Today's Todo`
3. `Publications`
4. `Reading Queue`

이 구성이 좋은 이유는 각 섹션의 역할이 명확하기 때문이다.

- `Active Projects`는 현재 내가 운영 중인 연구 라인을 보여준다
- `Today's Todo`는 오늘 바로 손을 대야 하는 실행 항목을 기록한다
- `Publications`는 이미 낸 실적을 별도 데이터베이스로 축적한다
- `Reading Queue`는 아직 다 읽지 않은 논문 큐를 유지한다

즉, 이 대시보드는 “연구의 현재”와 “연구의 축적”을 한 화면에 같이 올려놓는 구조다.

## 1. Active Projects: 지금 움직이는 연구를 한눈에 보기

`Active Projects` 섹션은 `04_Projects` 아래의 프로젝트 허브들을 Dataview로 불러오는 테이블이다. 여기서는 프로젝트 자체를 다시 설명하기보다, 지금 운영 중인 상태를 빠르게 스캔하는 것이 중요했다.

표에는 다음 정보가 들어간다.

- 프로젝트명
- 단계
- 건강도
- 우선순위
- 현재 포커스
- 다음 리뷰 날짜
- 목표 날짜
- 최근 업데이트 날짜

이 정보는 프로젝트 허브의 frontmatter에 이미 존재하므로, `PhD Dashboard`는 이를 다시 입력하지 않고 보여주기만 한다. 이 원칙이 중요하다. 최상위 대시보드는 데이터를 복제하지 않고, 각 허브의 최신 상태를 모아서 보여주는 뷰여야 한다.

## 2. Today's Todo: 가장 단순한 방식으로 남기는 일일 실행 화면

이번 작업에서 일부러 가장 심플하게 둔 부분이 `Today's Todo`다. Dataview나 Task 쿼리로 자동화할 수도 있지만, 지금 필요한 것은 자동 분류보다 빠른 입력이었다.

그래서 `Today's Todo`는 대시보드 안에 직접 체크리스트를 적는 방식으로 두었다. 이렇게 하면 하루를 시작할 때 다른 노트로 이동할 필요 없이, 바로 그 화면에서 오늘 해야 할 일을 적고 지울 수 있다.

이 방식의 장점은 세 가지다.

- 입력 비용이 매우 낮다
- 오늘의 우선순위를 직접 다시 쓰게 되므로 실행 감각이 살아난다
- 다른 시스템과 억지로 연동하지 않아도 된다

박사과정에서는 할 일이 너무 많아서, 자동화보다 “오늘 내가 실제로 잡고 갈 것”을 명확히 쓰는 편이 훨씬 중요할 때가 많다.

## 3. Publications: 실적 논문을 paper database와 분리한 이유

이번에 새로 정리한 핵심은 `Publications` 섹션이다. 기존의 `Papers`는 읽기와 리뷰를 위한 공용 문헌 데이터베이스이고, `Publications`는 내가 실제로 낸 성과를 저장하는 별도 데이터베이스다. 둘은 성격이 다르기 때문에 분리하는 편이 훨씬 낫다.

현재 구조는 다음처럼 나뉜다.

- `02_Sources/Papers`: 읽을 논문, 읽는 중인 논문, 정리 중인 논문
- `02_Sources/Publications`: 내 실적 논문

이 분리 덕분에 문헌 큐와 실적 아카이브가 서로 섞이지 않는다. 읽기용 paper note에는 `summary`, `limitations`, `reading_status` 같은 필드가 중요하지만, publication note에는 venue, 저자, PDF 링크, DOI 같은 출판 정보가 더 중요하다.

그래서 publication note는 별도 템플릿으로 관리하도록 했다. 현재 publication note에는 다음과 같은 정보가 들어간다.

```yaml
title: "논문 제목"
type: publication
status: published
created: "2026-04-07"
updated: "2026-04-07"
publication_year: 2026
venue_short: "ICASSP '26"
venue: "ICASSP 2026"
authors: "Author A, Author B"
projects: []
pdf_url: "https://..."
doi_url: "https://doi.org/..."
code_url:
notes:
tags:
  - publication
summary:
```

즉, publication note는 “읽기 메모”가 아니라 “성과 기록”에 맞춰 설계된 구조다.

## Publications 표는 어떻게 보이게 했나

`PhD Dashboard`에서 `Publications` 섹션은 다음 정보를 표로 보여준다.

- `Title`
- `Conf.`
- `Author`
- `File`
- `DOI`

이 구성을 선택한 이유는 이미지 없이도 한눈에 실적 목록을 읽을 수 있기 때문이다. 제목과 venue만 봐도 어떤 성과인지 빠르게 인식할 수 있고, 필요하면 PDF와 DOI로 바로 이동할 수 있다.

특히 이번에는 정렬 기준을 `updated DESC`로 두었다. 즉, 가장 최근에 수정한 publication note가 맨 위로 올라온다. 실적 노트는 완성 후에도 링크나 정리 문구를 보완하는 일이 자주 있기 때문에, 최신 작업이 위로 보이는 편이 더 실용적이다.

## 4. Reading Queue: Literature Dashboard와 이어지는 현재형 문헌 큐

`Reading Queue`는 공용 `Papers` 데이터베이스에서 `reading_status != "done"`인 항목만 가져오는 섹션이다. 이 섹션의 목적은 단순하다. 박사과정 전체 조종석에서도 지금 읽어야 할 논문을 바로 볼 수 있게 만드는 것이다.

즉, `Literature Dashboard`가 문헌 전용 작업 화면이라면, `PhD Dashboard`의 `Reading Queue`는 그중에서도 지금 미완료인 항목만 요약해서 보여주는 상위 뷰다.

표 컬럼은 literature dashboard와 동일하게 맞췄다.

- `Title`
- `Date`
- `Journal`
- `Status`
- `Summary`
- `Limitations`
- `Link`
- `Category`

같은 데이터베이스를 서로 다른 깊이에서 보는 구조를 유지해야, 대시보드 간 역할 분리가 자연스럽다.

## 버튼을 붙인 이유: 대시보드는 입력 인터페이스이기도 해야 한다

이번 정리에서 만족스러웠던 부분 중 하나는 버튼 기반 입력 흐름이다. `PhD Dashboard`에는 두 개의 버튼을 붙였다.

- `New Publication Note`
- `New Paper Note`

이 버튼을 누르면 각각 올바른 폴더에 새 노트가 생성되고, 템플릿도 자동 적용된다.

- publication은 `02_Sources/Publications`로 들어간다
- paper는 `02_Sources/Papers`로 들어간다

이 작은 차이가 실제 사용성에서는 꽤 크게 작용한다. 입력 경로가 한 번에 연결되어 있으면, “나중에 정리해야지” 하고 미루는 일이 줄어든다. 결국 데이터베이스는 구조보다 입력 마찰이 낮을 때 유지된다.

## 최종적으로 좋아진 점

지금 상태의 `PhD Dashboard`에서 가장 만족스러운 변화는 다음과 같다.

### 1. 상위 화면의 역할이 분명해졌다

`PhD Dashboard`는 연구 운영 화면이고, `Literature Dashboard`는 문헌 작업 화면이다. 둘의 기능이 겹치지 않는다.

### 2. Publications가 독립된 축으로 자리 잡았다

이전에는 읽는 논문과 낸 논문이 같은 층위에서 보일 여지가 있었는데, 이제는 실적 관리가 분리되어 훨씬 선명하다.

### 3. 오늘 할 일과 장기 축적이 같은 화면에 놓였다

당장 처리할 작업과 축적된 연구 성과가 한 화면에 있으면, 하루의 실행도 빠르고 연구의 방향감도 덜 잃게 된다.

### 4. 새 노트를 추가하는 비용이 계속 낮아졌다

문헌도, publication도 버튼 한 번으로 생성되기 때문에 시스템이 점점 더 실제 작업 흐름에 가까워지고 있다.

## 이 대시보드가 박사과정 운영에서 중요한 이유

박사과정은 한 가지 일만 깊게 하는 시간이 아니라, 여러 층위의 일을 동시에 다루는 시간에 가깝다. 읽어야 할 논문이 있고, 돌아가고 있는 프로젝트가 있고, 정리해야 할 실적이 있고, 오늘 마감해야 하는 일이 있다.

그래서 최상위 대시보드는 멋진 화면이 아니라, 전환 비용을 줄이는 장치여야 한다. 지금의 `PhD Dashboard`는 그 기준에 맞게 점점 단순해지고 있다.

결국 내가 원하는 것은 이런 화면이다.

- 지금 무엇이 진행 중인지 보이고
- 오늘 무엇을 해야 하는지 적을 수 있고
- 지금까지의 실적이 정리되어 있으며
- 다음에 읽을 논문이 바로 보이는 화면

이번 작업은 그 기준에 꽤 가까이 간 정리였다.

## 마무리

이번 `PhD Dashboard` 작업은 새로운 기능을 많이 붙이는 작업이 아니라, 박사과정 연구의 상위 조종석을 단순하고 강하게 만드는 작업이었다.

정리하면 현재 구조는 이렇게 나뉜다.

- `Literature Dashboard`: 공용 문헌 데이터베이스를 프로젝트별로 탐색하는 화면
- `PhD Dashboard`: 프로젝트, 오늘 할 일, 실적, 읽기 큐를 함께 운영하는 화면

이제 상위 대시보드 두 개의 역할이 거의 정리된 만큼, 앞으로는 개별 프로젝트 허브와 개념 레이어를 더 정교하게 다듬는 쪽으로 발전시켜볼 생각이다.
