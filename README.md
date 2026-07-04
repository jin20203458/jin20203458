# Jin (naneunmuneo)
**Software Engineer | Compiler Infrastructure | AI Pipelines & Architecture**

[![GitHub stats](https://github-readme-stats.vercel.app/api?username=jin20203458&show_icons=true)](https://github.com/jin20203458/github-readme-stats)

---

## About Me

LLVM/Clang 기반 정적분석 소프트웨어 **"ARQA Static"**의 메인 소프트웨어 엔지니어입니다. 
저수준 컴파일러 인프라 가공부터 비동기 데스크톱 어플리케이션 아키텍처 설계, 그리고 최신 AI 연동 파이프라인까지 아우르는 풀스택 시스템 설계 및 개발에 주력하고 있습니다.

- **Focus**: System Architecture, Compiler Infrastructure (LLVM/Clang), AI Ecosystem Engine, Asynchronous Programming
- **Philosophy**: "자유도 높은 시스템 속에서 통제 가능한 질서를 설계합니다."

---

## Tech Stack

- **Languages**: C++, C#
- **Infrastructure & Frameworks**: LLVM/Clang, .NET, Unity, gRPC

---

## Key Projects

### Project Mundus Vivens (AI NPC 자율 생태계 엔진)
*LLM의 자유도와 게임 시스템의 통제 가능성을 결합한 시뮬레이션 시스템*

- **Architecture**: 
  - **C++ Game Server**: 물리 연산 및 공간 논리를 담당하는 3-스레드 리액터 모델
  - **C# AI API Server**: 인지 모델 및 LLM 통신을 전담하는 백엔드 서버
  - **Unity Client**: TCP 통신을 통해 월드를 렌더링하는 클라이언트
  - *서버 간 통신은 고성능 gRPC 파이프라인으로 통합 운영됩니다.*
- **Features**:
  - **통합 믿음(Belief) 엔진**: NPC들이 상호작용을 통해 단기/중기/장기(Core) 기억을 형성하고, 시간에 따른 자연스러운 쇠퇴(Decay) 및 와전(Mutation)을 수학적으로 시뮬레이션합니다.
  - **자율 동적 관계망**: 플레이어 개입 없이도 공간 조우 기반으로 대화 확률을 계산하며, 스스로 호감도 및 신뢰도를 갱신하고 일일 스케줄 성찰(Reflection)을 수행합니다.

### GRC (Gemini Roleplay Chat)
*고몰입도 캐릭터 AI 롤플레잉 및 소설 창작용 데스크톱 클라이언트*

- **Environment**: WPF, C# (.NET 8.0)
- **Features**:
  - **3단계 압축 기억 메커니즘**: 대규모 서사를 장기간 유지하기 위한 계층형 메모리 구조 (Raw History / Chapter Plot / Chronicle).
  - **AI 세션 아키텍트**: 에이전트 기반 자율 TRPG 세션 빌더 및 자율 감사관(Auditor) 루프 구현.
  - **감정선 반영 TTS**: Gemini 멀티모달 오디오를 활용하여 평행세계 분기 시스템 및 감정 상태에 따른 음성 연출.

### MCP Context Feeder & AiAgent.Diagnostics
*AI 에이전트 생산성 및 자율 디버깅을 위한 보조 파이프라인*

- **MCP Context Feeder**: 로컬 JSON-RPC/SSE 기반으로 옵시디언(Obsidian)과 연동하여 AI 에이전트의 컨텍스트 참조 효율을 극대화합니다.
- **AiAgent.Diagnostics**: AI 에이전트가 런타임 오류를 자율 분석하고 스스로 소스 코드를 수정할 수 있도록 설계된 고성능 비침투적 관찰(Observability) 모듈.

---

## Contact

- **Email**: adg01008@naver.com
- **GitHub**: [jin20203458](https://github.com/jin20203458)
- **Solved.ac**: [naneunmuneo](https://solved.ac/naneunmuneo/)
