# Simplicity is the Ultimate Sophistication

**복잡함 속 단순함을 추구하는 개발자 이진우입니다.**

기술을 무분별하게 더하기보다, CS 지식과 데이터를 근거로 최적의 추상화를 설계하는 과정을 즐깁니다.

> 서울과학기술대학교 재학 (3학년) · **백엔드 엔지니어**를 목표로 Spring 기본기와 알고리즘을 매일 기록하며 학습 중입니다.

[![Tech Blog](https://img.shields.io/badge/Tech%20Blog-11B48A?style=flat-square&logo=velog&logoColor=white)](https://velog.io/@snowmile1224/posts)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/%EC%A7%84%EC%9A%B0-%EC%9D%B4-484bab3a3/)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:enderpawar@naver.com)

---

##  Daily Practice

매일 세 가지를 **기록으로** 남깁니다. 말보다 흔적으로 증명하는 편을 선호합니다.

| 트랙 | 내용 | 기록 |
|---|---|---|
| **Algorithm** | 하루 2~3문제 + 풀이 회고 | [LeetCode-75](https://github.com/enderpawar/LeetCode-75) |
| **Backend** | Spring 기본기 8주 커리큘럼 | [`[백엔드 기본기]` 시리즈](https://velog.io/@snowmile1224/posts) |
| **Writing** | 학습 과정을 매일 정리 | [Tech Blog](https://velog.io/@snowmile1224/posts) |

###  최근 작성한 글

<!-- BLOG-POST-LIST:START -->
<!-- BLOG-POST-LIST:END -->

강의 요약이 아니라 **직접 실행해 검증한 기록**을 씁니다.
`문제 → 순진한 시도 → 에러 → 수정 → 개념 정리` 구조로 작성합니다.

<details>
<summary>예시: 왜 이 구조로 쓰는가</summary>

`@Valid` 검증 실패 시 응답을 예측해보고 실제로 찍어봤더니, 예상과 달리 메서드 본문이 아예 실행되지 않았습니다.
`MethodArgumentNotValidException`이 **본문 진입 전에** 던져지기 때문이었습니다.
"동작한다"에서 멈추지 않고 **"왜 이 시점인가"** 까지 확인해야 다음에 응용할 수 있다고 생각합니다.

</details>

---

##  Engineering Philosophy

> "내부 로직을 간단하고 직관적으로 만들어 팀과 사용자에게 명료함을 전달"

- **Evidence-based Design** — 취향이 아니라 데이터와 제약 조건(성능·비용·저장 공간)으로 결정합니다.
  → *CS-NextDoor에서 36개 파라미터 조합을 실측 비교해 전처리 파이프라인을 확정했습니다.*
- **Simplicity over Complexity** — 동료가 1분 안에 이해할 수 있는 로직을 우선합니다.
- **Documenting 'Why'** — 결정의 근거를 남깁니다. 학습 과정은 [기술 블로그](https://velog.io/@snowmile1224/posts)에,
  코드 변경의 의도는 PR 본문에 `[Design Decision]` 형식으로 기록합니다.
- **결과를 과장하지 않기** — 측정했다면 표본 수와 한계도 함께 적습니다.

---

##  Tech Stack

현재 **프로젝트에 적용해본 것**과 **학습 중인 것**을 구분해 적었습니다.

| Category | 프로젝트 적용 경험 | 학습 중 (2026 H2) |
|---|---|---|
| **Backend** | Spring Boot (REST API 설계·SSE 스트리밍), Node.js | JPA, 트랜잭션, Spring Security |
| **Frontend** | React, TypeScript, Vite, Electron | Next.js |
| **CV / AI** | OpenCV (Python · WASM), Gemini Vision API | — |
| **Infra** | GitHub Actions, Vercel, Railway | Docker, PostgreSQL, Redis |

---

## 📂 Featured Projects

### 1. CS-NextDoor | OpenCV × Gemini 기반 PC 진단 가이드
<img width="1151" height="1638" alt="image" src="https://github.com/user-attachments/assets/ebbc5f80-2809-4253-a04e-91bb5b17ec92" />

> "텍스트 안내는 있는데, 화면에서 그게 어디인지 모르는 문제"

[📂 Repository](https://github.com/enderpawar/CS-NextDoor) · [🔗 Live Demo](https://nextdoor-cs.vercel.app) · `React PWA` `Spring Boot` `OpenCV.js` `Gemini Vision`

- **Problem** — 비전문가는 "Boot Priority를 바꾸세요"라는 안내를 읽어도 BIOS 화면에서 해당 항목을 찾지 못합니다.
- **Solution** — 역할을 명확히 분리했습니다. **OpenCV는 "어디"(픽셀 좌표), LLM은 "무엇"(의미 판단)** 을 담당합니다.
  화면 정규화(Canny → Hough → Homography → CLAHE) 후, 히스토그램 변화 감지로 **필요한 순간에만** LLM을 호출합니다.
- **Results**
  - 파라미터 36개 조합 실측 비교(ablation)로 전처리 단계 확정
  - 불필요한 API 호출 제거 → **호출량 83% 감소, 시간당 $1.50 → $0.26**
  - 실촬영 BIOS 22장으로 ROI 검출 검증
- **한계 (명시)** — 품질 필터 ROC는 n=13 소표본이고, ROI 개수는 OCR 정확도의 대리 지표입니다. 결론을 일반화하지 않았습니다.

### 2. TRADE BUILDER | 노드 기반 자산 운용 자동화
<img width="3822" height="2018" alt="image" src="https://github.com/user-attachments/assets/b15de7a1-390d-4d2b-9ca6-989a8a0ac9a2" />

> "초당 수천 건의 틱 데이터를 핵심 시그널로 단순화하기"

[📂 Repository](https://github.com/Trade-Builder/Trade-Builder-Client) · `Electron` `React 19` `TypeScript` `Rete.js` `Upbit API`

- **Problem** — 고빈도 틱 데이터를 그대로 렌더링하면 클라이언트에서 병목이 발생했습니다.
- **Solution** — 데이터 파이프라인에서 핵심 시그널만 추출하고, 컴포넌트를 Atomic 단위로 분리해 갱신 범위를 좁혔습니다.
- **Results** — **UI 리렌더링 20% 감소, 메모리 점유 약 25% 절감**
- **다음 단계** — 매매 로직 단위 테스트 및 백테스트 추가 (실자산이 움직이는 도메인이라 검증 우선순위가 가장 높습니다)

### 3. CREATIVE AI | 노드 기반 비주얼 AI 파이프라인 에디터
<img width="2560" height="1347" alt="image" src="https://github.com/user-attachments/assets/30e44352-fa77-469e-977d-b81fcc131d37" />

> "복잡한 AI 로직을 직관적인 노드로 시각화"

[📂 Repository](https://github.com/enderpawar/CREATIVE_AI) · [🔗 Live Demo](https://enderpawar.github.io/CREATIVE_AI/) · `React 19` `TypeScript` `Rete.js v2` `Gemini API`

- **Problem** — 사용자가 노드를 자유롭게 연결하면 순환 참조로 무한 루프와 크래시가 발생할 수 있었습니다.
- **Solution** — 실행 **전에** DFS 기반 정적 분석으로 순환 구조를 감지해 차단했습니다.
- **Results** — 런타임 무한 루프 0건 / 파이프라인을 Python·Jupyter 코드로 내보내기 지원

---

## 🤝 How I Work

- **PR 기반 개발** — 개인 프로젝트도 브랜치 → PR → 리뷰 흐름으로 진행하고, 결정 근거를 본문에 남깁니다.
- **Why-Driven Review** — 코드 리뷰에서 스타일보다 의도와 맥락을 먼저 확인합니다.
- **AI 활용 기준** — 보일러플레이트와 반복 작업은 AI로 줄이고, **아키텍처 결정과 성능 측정은 직접** 합니다.
  CS-NextDoor의 ablation 실험 설계처럼, 판단이 필요한 부분은 근거를 만들어 결정합니다.
