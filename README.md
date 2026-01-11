# 🚀 Simplicity is the Ultimate Sophistication

안녕하세요, **복잡함 속 단순함을 추구하는 개발자 이진우**입니다.  
복잡한 엔지니어링 문제를 만났을 때 기술을 무분별하게 더하기보다, CS 지식과 데이터를 근거로 최적의 추상화를 설계하는 과정을 즐깁니다.

<p align="left">
  <a href="https://velog.io/@snowmile1224/posts"><img src="https://img.shields.io/badge/Tech%20Blog-11B48A?style=flat-square&logo=velog&logoColor=white" /></a>
  <a href="https://www.linkedin.com/in/%EC%A7%84%EC%9A%B0-%EC%9D%B4-484bab3a3/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:enderpawar@naver.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white" /></a>
</p>

---

## 💡 Engineering Philosophy

> **"복잡한 내부 로직을 어떻게 간단하고 직관적으로 만들 수 있을까에 집중하여, 동료와 사용자에게 명료함을 전달합니다."**

* **Evidence-based Design:** "왜 이 기술인가?"에 대해 막연한 선호도가 아닌 **데이터와 제약 조건(Storage, 성능, 비용)**을 근거로 의사결정합니다.
* **Simplicity over Complexity:** 오버 엔지니어링을 경계합니다. 동료 누구나 1분 안에 이해할 수 있는 명확한 로직이 가장 효율적인 코드라고 믿습니다.
* **Documenting 'Why':** 코드 자체보다 '왜 그렇게 작성했는가'에 대한 맥락을 중요시합니다. 모든 주요 의사결정은 **[Design Decision]** 태그와 함께 Issue/PR에 기록하여 협업 비용을 최소화합니다.

---

## 🛠 Tech Stack & Reasoning


| Category | Tech Stack | Reason for Choice |
| :--- | :--- | :--- |
| **Frontend** | React, Next.js, TS | 타입 안정성을 기반으로 대규모 프로젝트의 유지보수성을 확보하고 SEO 최적화 고려. |
| **Backend** | Node.js, Spring Boot | 빠른 프로토타이핑(Node.js)과 대규모 트래픽 하의 안정적 트랜잭션 처리(Spring)를 병행. |
| **Database** | PostgreSQL, Redis | 데이터 정합성 보장(PostgreSQL) 및 실시간 데이터 캐싱을 통한 Latency 최소화(Redis). |
| **Tools** | Docker, GH Actions | 환경 일관성 유지 및 CI/CD 자동화를 통한 휴먼 에러 방지와 배포 속도 개선. |

---

## 📂 Featured Projects

### 1. CREATIVE AI | 노드 기반 비주얼 AI 파이프라인 에디터
<img width="3839" height="1968" alt="image" src="https://github.com/user-attachments/assets/391eb0ae-743a-4634-8f4a-730471769f97" />

> **"복잡한 AI 로직을 직관적인 노드 인터페이스로 시각화하여 설계 진입 장벽 최적화"** > [📂 Repository](https://github.com/enderpawar/CREATIVE_AI) | [🔗 Live Demo](https://enderpawar.github.io/CREATIVE_AI/)

* **Problem:** 사용자의 자유로운 노드 연결로 인한 **순환 참조(Circular Reference)** 발생 시, 실행 단계에서 무한 루프 및 브라우저 크래시 위험 존재.
* **Solution:** * **Graph Algorithm:** DFS(Depth-First Search) 기반의 정적 분석 로직을 구현하여 파이프라인 실행 전 순환 구조를 사전에 감지.
    
    * **State Management:** 복잡한 노드 상태를 JSON 구조로 직렬화하여 Local Storage와 동기화, 자동 저장 기능 구현.
* **Key Results:**
    * 런타임 무한 루프 발생 가능성 **0% 달성**.
    * 노드 배치 데이터 모듈화를 통해 코드 재사용성 및 가독성 향상.

---

### 2. TRADE BUILDER | 전략적 자산 운용 자동화 시스템
<img width="3822" height="2018" alt="image" src="https://github.com/user-attachments/assets/e7110cd4-3cbb-43a0-a0b3-02cba3f9ac1f" />

> **"방대한 시장 데이터를 핵심 지표로 단순화하여 사용자 중심의 자동화 환경 구축"** > [📂 Repository](https://github.com/Trade-Builder/Trade-Builder-Client)

* **Problem:** 실시간 유입되는 초당 수천 건의 **틱 데이터(Tick Data)** 처리 시 클라이언트 렌더링 병목 및 메모리 과부하 발생.
* **Solution:**
    * **Data Pipeline:** 원시 데이터를 그대로 노출하지 않고, Redis를 거쳐 전략 실행에 필요한 **핵심 시그널(Signal)만 추출**하는 필터링 파이프라인 설계.
    
    * **Optimization:** `React.memo` 및 Atomic Design 기반 UI 컴포넌트 설계를 통한 불필요한 리렌더링 방지.
* **Key Results:**
    * 데이터 처리 최적화로 **UI 리렌더링 20% 감소** 및 시각적 노이즈 제거.
    * 시스템 **메모리 점유율 약 25% 절감**으로 저사양 환경에서도 안정적인 모니터링 보장.
    * **PostgreSQL** 격리 수준(Isolation Level) 조정을 통해 대량 매매 요청 시 데이터 정합성 확보.

---

## 📈 Daily & Collaborative Habit

* **Continuous Learning:** 매일 알고리즘 문제 풀이를 통해 복잡한 문제를 논리적으로 쪼개는 훈련을 지속합니다.
* **Why-Driven Review:** 코드 리뷰 시 '어떻게(How)'보다 **'왜(Why)'**에 집중하여 트러블 슈팅에 대응할 수 있을 기술적 성장을 도모합니다.
* **AI Pair Programming:** Cursor 또는 Copilot를 적극 활용해 반복적인 코드를 줄이고, 고차원적인 비즈니스 로직 설계에 집중합니다.

---
