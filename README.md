<p align="center">
  <img src="./shadow-clone.jpeg" alt="Shadow Clone Jutsu" width="600"><br><br>
  <h1 align="center">Shadow Clone (그림자 분신술)</h1>
  <p align="center">
    <strong>Claude Code Skill for Intelligent Parallel Agent Orchestration</strong><br>
    정찰하고 &middot; 분해하고 &middot; 병렬 실행하고 &middot; 통합 검증합니다
  </p>
</p>

<p align="center">
  <a href="#설치">설치</a> &nbsp;&bull;&nbsp;
  <a href="#커맨드">커맨드</a> &nbsp;&bull;&nbsp;
  <a href="#사용-예시">사용 예시</a> &nbsp;&bull;&nbsp;
  <a href="#라이선스">라이선스</a>
</p>

---

## 설치

```
/install-plugin https://github.com/nathankim0/shadow-clone
```

---

## 커맨드

### `shadow-clone` — 지능형 병렬 에이전트 오케스트레이션

나루토의 그림자 분신술처럼 각 분신이 독립적으로 작업하고, 소멸 시 기억(결과)이 본체에게 돌아오는 구조.

```
/shadow-clone:shadow-clone [에이전트 수] <작업 지시>
```

### 4단계 파이프라인

| Phase | 이름 | 설명 |
|-------|------|------|
| 1 | **정찰 (偵察)** | Explore 에이전트로 프로젝트 구조, 파일 분포, 의존성 파악 |
| 2 | **분해 (分解)** | 최적 분해 전략 선택 + 배타적 파일 소유권 할당 |
| 3 | **실행 (実行)** | N개 분신을 병렬 소환하여 독립 작업 수행 |
| 4 | **통합 (統合)** | 결과 수집 + 충돌 감지 + 품질 검증 + 최종 보고 |

### 분해 전략

| 전략 | 언제 사용 | 예시 |
|------|----------|------|
| **파일/모듈별** | 독립적 모듈이 명확할 때 | 각 에이전트가 다른 패키지/디렉토리 담당 |
| **관심사별** | 횡단 관심사가 있을 때 | 테스트/타입/로직/스타일 각각 담당 |
| **역할별** | 복합 작업일 때 | 탐색자 + 구현자 + 검증자 |
| **단계별** | 의존성이 있을 때 | 1차: 인터페이스 설계 → 2차: 구현 |

### 분신별 모델 자동 매칭

각 분신의 작업 복잡도에 따라 최적 모델이 개별 배정됩니다:

| 작업 성격 | 모델 | 이유 |
|----------|------|------|
| 단순 탐색, 파일 검색, 구조 파악 | `haiku` | 속도 우선 |
| 코드 분석, 패턴 탐지, 리뷰 | `sonnet` | 분석 정확도 필요 |
| 코드 작성, 수정, 리팩토링 | `sonnet` | 충분한 코드 품질 |
| 아키텍처 설계, 복잡한 로직 구현 | `opus` | 높은 추론 능력 필요 |
| 빌드, 테스트 실행, 단순 스크립트 | `haiku` | 속도 우선 |

### 차별점: 일반 에이전트 호출 vs 그림자 분신술

| 일반 에이전트 호출 | 그림자 분신술 |
|---|---|
| "에이전트 3개 띄워줘" | 정찰 → 분석 → 최적 분해 → 배타적 할당 → 실행 → 검증 |
| 작업 범위 겹침 가능 | 파일/디렉토리 소유권 배타적 할당으로 충돌 제로 |
| 한 번에 끝 | 다중 웨이브: 1차 결과 기반 2차 배치 가능 |
| 결과 그냥 나열 | 결과 통합 + 충돌 해결 + 품질 검증 |
| 에이전트 타입 수동 선택 | 서브태스크별 최적 에이전트 타입 자동 매칭 |
| 모든 에이전트 동일 모델 | 분신별 작업 성격에 따라 haiku/sonnet/opus 개별 배정 |

---

## 사용 예시

<details>
<summary><b>아키텍처 분석</b></summary>

<br>

```
> /shadow-clone:shadow-clone 이 프로젝트의 아키텍처를 완전히 분석해줘
```

#### Phase 1: 정찰
```
프로젝트 구조 파악 중...
- src/: 메인 소스 (45 파일)
- tests/: 테스트 (12 파일)
- 기술 스택: TypeScript, React, Vite
```

#### Phase 2: 분해 — 파일/모듈별 전략, 4개 분신

| 분신 | 타입 | 모델 | 담당 영역 |
|------|------|------|----------|
| clone-1 | Explore | haiku | src/components/ |
| clone-2 | Explore | haiku | src/hooks/ + src/utils/ |
| clone-3 | Explore | sonnet | src/api/ + src/store/ |
| clone-4 | Explore | haiku | src/pages/ + src/routes/ |

#### Phase 3: 실행 — 4개 분신 병렬 소환

#### Phase 4: 통합 보고
```
투입 전력: 4개 분신, 파일/모듈별 전략
충돌: 없음, 누락: 없음, 품질: 통과
```

</details>

<details>
<summary><b>Deprecated API 수정</b></summary>

<br>

```
> /shadow-clone:shadow-clone 5 src/ 전체에서 deprecated API를 찾아 수정해줘
```

#### Phase 1: 정찰
```
deprecated API 사용 파일 탐색 중...
- 15개 파일에서 deprecated API 사용 발견
```

#### Phase 2: 분해 — 파일별 배타적 할당, 5개 분신

| 분신 | 타입 | 모델 | 배타적 파일 |
|------|------|------|-----------|
| clone-1 | general-purpose | sonnet | file1.ts, file2.ts, file3.ts |
| clone-2 | general-purpose | sonnet | file4.ts, file5.ts, file6.ts |
| clone-3 | general-purpose | sonnet | file7.ts, file8.ts, file9.ts |
| clone-4 | general-purpose | sonnet | file10.ts, file11.ts, file12.ts |
| clone-5 | general-purpose | sonnet | file13.ts, file14.ts, file15.ts |

#### Phase 3: 실행 — 5개 분신 병렬 수정

#### Phase 4: 충돌 검증 + 통합 보고

</details>

---

## 에이전트 작업 추적

각 분신은 임시 작업 계획 파일(`/tmp/shadow-clone-{timestamp}/clone-plan-{N}.md`)을 생성하여 작업 진행 상황을 기록합니다. 중간에 오류로 중단되더라도 이 파일을 통해 작업을 재개할 수 있습니다.

---

## 라이선스

[MIT](./LICENSE)
