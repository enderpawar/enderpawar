
[![Solved.ac 프로필](http://mazassumnida.wtf/api/v2/generate_badge?boj=enderpawar)](https://solved.ac/enderpawar)
# 🚀 Simplicity is the Ultimate Sophistication

안녕하세요, **단순함의 본질에 집중하는 개발자 이진우**입니다.  
복잡한 문제를 만났을 때 기술을 더하기보다, **비즈니스 가치를 극대화할 수 있는 가장 단순하고 명확한 해답**을 설계하는 과정을 즐깁니다.

---

### 💡 Engineering Philosophy

* **Simplicity over Complexity**: 오버 엔지니어링을 경계합니다. 동료 누구나 1분 안에 이해할 수 있는 명확한 로직이 가장 효율적인 코드라고 믿습니다.
* **Evidence-based Design**: "왜 이 기술인가?"에 대해 막연한 선호도가 아닌 **데이터와 제약 조건(Storage, 성능, 비용)**을 근거로 의사결정합니다.
* **Collaborative Growth**: 기록을 무엇보다 중요시하여, 의사결정 과정을 Issue와 PR에 상세히 기록하고 팀의 커뮤니케이션 비용을 낮추는 데 집중합니다.

---

### 🛠 Tech Stack & Tools

| Category | Tech Stack |
| :--- | :--- |
| **Frontend** | React, Next.js, TypeScript, Tailwind CSS |
| **Backend** | Node.js, Java, Spring Boot |
| **Database** | PostgreSQL, Redis, MongoDB | 
| **Tools** | Git, GitHub Actions, Docker, Cursor/Claude (AI Pair Programming) |

---

### 📂 Featured Projects

#### 1. [CREATIVE AI](https://github.com/enderpawar/CREATIVE_AI) | 노드 기반 비주얼 AI 파이프라인 에디터
> **"추상적이고 복잡한 AI 로직을 직관적인 노드 인터페이스로 시각화하여 설계 진입 장벽을 낮춤"**

* **Project Goal**: 텍스트 기반 AI 코딩의 복잡성을 제거하고, 드래그 앤 드롭 방식의 노드 배치를 통해 누구나 쉽게 고도화된 AI 파이프라인을 설계할 수 있는 환경 제공.
* **Challenge**: 사용자가 자유롭게 노드를 연결하는 과정에서 **순환 참조(Circular Reference)**가 발생할 경우, 파이프라인 실행 시 시스템 무한 루프에 빠져 브라우저가 크래시되는 치명적인 사용자 경험 저하 위험이 존재함.
* **Solution**: **DFS(Depth-First Search) 알고리즘** 기반의 정적 분석 로직을 구현. 파이프라인 실행 전 그래프 전체를 탐색하여 순환 구조를 사전에 감지하고 차단함으로써 시스템 안정성을 확보.
* **Key Results**: 
    * 실행 전 검증 프로세스 도입으로 런타임 무한 루프 발생 가능성 **0% 달성**.
    * 노드 배치 데이터를 효율적인 JSON 구조로 직렬화하여, 복잡한 설계도 Local Storage 내에 **안정적으로 자동 저장**.
    * 복잡한 AI 로직을 최소 단위 노드로 모듈화하여 코드 재사용성 및 가독성 향상.
* **Insight**: 시각적 자유도가 높은 툴일수록 이면의 논리적 제약(Constraint)이 견고해야 함을 깨달았으며, 사용자에게는 '단순함'을 주되 시스템은 '정교함'을 유지해야 한다는 엔지니어링 원칙을 정립함.

#### 2. [TRADE BUILDER](https://github.com/Trade-Builder/Trade-Builder-Client) | 전략적 자산 운용 자동화 시스템
> **"복잡한 주식 매매 전략을 핵심 지표 위주로 단순화하여 사용자 중심의 자동화 환경 구축"**

* **Project Goal**: 전문가 영역으로 여겨졌던 복잡한 주식 매매 전략 수립 과정을 추상화하여, 일반 사용자도 직관적으로 자신만의 자산 운용 로직을 구축하고 자동화할 수 있는 인터페이스 제공.
* **Challenge**: 실시간으로 유입되는 방대한 양의 시장 데이터(Tick data)와 복잡하게 얽힌 매매 조건들이 결합될 경우, 사용자가 정보 과부하를 겪을 뿐만 아니라 클라이언트 단에서 심각한 렌더링 병목 현상이 발생함.
* **Solution**: 데이터 흐름을 계층화하여 단순화. 원시 데이터(Raw data)를 그대로 노출하지 않고, 전략 실행에 필요한 **핵심 시그널(Signal)만 추출하는 필터링 파이프라인**을 설계하여 복잡한 로직을 시각적으로 명료하게 변환.
* **Key Results**: 
    * 데이터 처리 파이프라인 최적화로 불필요한 UI 리렌더링 **20% 감소** 및 시각적 노이즈 제거.
    * 매매 로직의 모듈화(Atomic Design)를 통해 사용자가 전략을 수정하고 검증하는 속도 개선.
    * 메모리 점유율 **약 25% 절감**으로 저사양 환경에서도 끊김 없는 실시간 데이터 모니터링 보장.
* **Insight**: 진정한 단순함은 기능을 줄이는 것이 아니라, **복잡한 내부 로직을 잘 설계된 추상화 뒤로 숨겨 사용자에게 필요한 정수만 전달하는 것**임을 깨달았습니다.

---

### 📈 Daily & Collaborative Habit

* **Continuous Learning**: 매일 알고리즘 문제 풀이와 기록을 통해 논리적 사고의 끈을 놓지 않습니다.
* **Documenting 'Why'**: 단순한 코드 작성을 넘어, **[Design Decision]**을 Issue에 기록하여 동료들이 코드의 맥락을 빠르게 파악할 수 있도록 돕습니다.

---

### 📫 Contact & Channels

* **Email**: enderpawar@naver.com
* **LinkedIn**: https://www.linkedin.com/in/%EC%A7%84%EC%9A%B0-%EC%9D%B4-484bab3a3/
* **Blog**: https://velog.io/@snowmile1224/posts

---
