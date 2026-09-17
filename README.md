
# Jin (naneunmuneo)
## About Me
정적분석 솔루션 [ARQA Static](https://kocome.com/solution)의 메인 시스템 엔지니어입니다.  
컴파일러 인프라 처리부터 비동기 데스크톱 아키텍처, 그리고 대규모 AI 파이프라인까지, 복잡한 비즈니스 요구사항을 고성능 아키텍처로 풀어내는 엔드투엔드(End-to-End) 시스템 엔지니어링에 집중하고 있습니다.
- **Core Focus**: 
  - **High-Performance & Kernel Systems**: Windows ETW 커널 텔레메트리 후킹 및 마이크로초(μs) 단위 지연 최소화를 위한 초저지연 액추에이션 설계
  - **Compiler Tooling**: LLVM/Clang 기반의 정적 분석(Static Analysis) 엔진 및 도구 체인 구축
  - **Concurrent Architecture**: 동시성 제어 및 논블로킹(Non-blocking) 기반의 확장 가능한 분산 서버/앱 아키텍처
  - **AI Orchestration & Observability**: 도구 호출(Tool Calling) 기반 자율 ReAct 수사 파이프라인, 비침투적 가관측성(Observability) 및 분산 환경에서의 자율 AI 에이전트 오케스트레이션
- **Engineering Philosophy**: *"자유도 높은 시스템 속에서 정밀하게 통제 가능한 질서를 설계합니다."*

---

## Technical Matrix

### Languages
<img src="https://img.shields.io/badge/C%2B%2B20-00599C?style=flat-square&logo=c%2B%2B&logoColor=white" /> <img src="https://img.shields.io/badge/C%23%2011.0-239120?style=flat-square&logo=c-sharp&logoColor=white" />

### OS & Kernel Internals
<img src="https://img.shields.io/badge/Windows%20ETW%20(Kernel)-0078D6?style=flat-square&logo=windows&logoColor=white" /> <img src="https://img.shields.io/badge/Win32%20Native%20API-00599C?style=flat-square&logo=windows&logoColor=white" /> <img src="https://img.shields.io/badge/MITRE%20ATT%26CK-ED1C24?style=flat-square&logo=shield&logoColor=white" /> <img src="https://img.shields.io/badge/DFIR%20(VAD%20Memory)-333333?style=flat-square&logo=target&logoColor=white" />

### Server Architecture & Profiling
<img src="https://img.shields.io/badge/EnTT%20(ECS)-00599C?style=flat-square&logo=c%2B%2B&logoColor=white" /> <img src="https://img.shields.io/badge/Tracy%20Profiler-FF6600?style=flat-square&logo=c%2B%2B&logoColor=white" />

### System & Infrastructure Core
<img src="https://img.shields.io/badge/LLVM/Clang%20Toolchain-111111?style=flat-square&logo=llvm&logoColor=white" /> <img src="https://img.shields.io/badge/gRPC-244c5a?style=flat-square&logo=grpc&logoColor=white" /> <img src="https://img.shields.io/badge/Protocol%20Buffers-3A6B4F?style=flat-square&logo=c&logoColor=white" /> <img src="https://img.shields.io/badge/TCP/IP%20Sockets-000000?style=flat-square&logo=internetexplorer&logoColor=white" /> <img src="https://img.shields.io/badge/Boost.Asio-00599C?style=flat-square&logo=boost&logoColor=white" />

### Data & AI Pipeline
<img src="https://img.shields.io/badge/LiteDB%20(NoSQL)-4CAF50?style=flat-square&logo=mongodb&logoColor=white" /> <img src="https://img.shields.io/badge/Google%20Gemini%20API-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" /> <img src="https://img.shields.io/badge/nlohmann/json-000000?style=flat-square&logo=json&logoColor=white" />

### Frameworks & Client
<img src="https://img.shields.io/badge/.NET%209.0-512BD4?style=flat-square&logo=dotnet&logoColor=white" /> <img src="https://img.shields.io/badge/WPF-3A96DD?style=flat-square&logo=windows&logoColor=white" /> <img src="https://img.shields.io/badge/Unity%203D-000000?style=flat-square&logo=unity&logoColor=white" />

### Build & Package Managers
<img src="https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white" /> <img src="https://img.shields.io/badge/vcpkg-181717?style=flat-square&logo=c&logoColor=white" />

---

## Pinned Projects

### Project Phalanx (AI-Augmented Windows Kernel EDR Solution)
*Windows 커널 텔레메트리 후킹과 자율 LLM ReAct 위협 헌터를 결합한 차세대 2-Tier 엔드포인트 탐지 및 대응 솔루션*

```mermaid
graph LR
    subgraph Kernel & Sensor Layer
        ETW[Windows Kernel ETW] -->|Hooking| Collector[EtwKernelCollector]
        Collector -->|Zero-Drop| Queue[DoubleBuffered<br/>SwapQueue]
        Actuator[ProcessActuator<br/>24μs NtSuspendProcess<br/>0.1ms TerminateProcess] -.->|Enforce| Target[Target Process]
        WD[SafetyWatchdog<br/>30s SLA / Auto-Resume] --> Actuator
    end

    subgraph IPC Pipeline
        Client[C++ GrpcStreamClient<br/>asio-grpc C++20]
        Queue --> Client
        Client <-->|gRPC Bidirectional Stream<br/>HTTP/2 Port 50051| Server[C# Kestrel Server<br/>PhalanxGrpcService]
        Server -.->|MitigationCommand| Client
        Client -.-> Actuator
    end

    subgraph Cognitive AI & Forensics
        Server --> Tree[ProcessTree<br/>Projection CQRS]
        Server --> Agent[AutonomousHunterAgent<br/>Gemini 3.8 Flash ReAct]
        Agent <--> LLM[(Google Gemini API<br/>JSON Mode)]
        Agent --> Tools[5 Forensic Tools<br/>VAD Scan / Decoder / Firewall]
        Agent --> Archive[(LiteDB Forensics<br/>Audit Storage)]
    end

    subgraph SecOps Cockpit
        Server --> Bridge[CockpitUiBridge<br/>Dispatcher Marshaling]
        Bridge --> WPF[WPF MainWindow<br/>Progressive Disclosure<br/>Forensic Inspector]
        Ctrl[SensorProcessController<br/>UAC runas & Local Event] -.->|Lifecycle| Client
    end
```

- **초저지연 커널 액추에이션 (Deterministic Reflex)**: Windows 커널 ETW 실시간 수집 및 `NtSuspendProcess`를 활용한 **24μs급 원자적 프로세스 동결** 구현. 랜섬웨어 시스템 파괴 명령 감지 시 0.1ms 이내 즉각 현장 사살 집행 (락 경합을 원천 차단한 더블 버퍼드 락-스왑 큐 및 30초 SLA SafetyWatchdog 자동 재개/연장 페일세이프 내장).
- **자율 ReAct AI 위협 헌터 (Gemini 3.8 Flash)**: 최대 5턴 제한 가드 기반의 자율 추론 루프로 5대 OS 수사 도구(VirtualQueryEx 기반 VAD Unbacked 실행 메모리 핀포인트 스캔, Gzip/Base64/Hex 다단계 난독화 해독, RFC 1918 사설망 마스킹 위협 평판, MITRE ATT&CK 26종 정규식 체계 분류, Windows 방화벽 C2 IP 격리)를 자율 오케스트레이션.
- **단일 진실 공급원(SSOT) 신뢰성 아키텍처**: 정적 문자열 휴리스틱이 AI의 결론을 왜곡하는 의사결정 탈취(Decision Hijacking)를 배제하고, ReAct 루프 완결 시 LLM 수사관의 최종 판결(`ACTION_KILL` vs `ACTION_RESUME`)을 100% 최상위 권한으로 수용하여 정상 관리 스크립트 오탐을 완벽 차단.
- **엔터프라이즈 WPF 관제 콕핏**: 이모티콘 0개의 절제된 Obsidian Dark 토큰 테마, 점진적 공개(Progressive Disclosure) 기반 마스터-디테일 포렌식 인스펙터, `runas` UAC 자동 기동 및 세션 로컬 Win32 명명 이벤트(`Local\PhalanxSensorShutdownEvent`)를 통한 고아 프로세스 없는 순차 동기 수명주기 제어.

---

### Project Mundus Vivens (AI AGENTS 자율 생태계 엔진)
*LLM의 높은 추론 자유도와 전통적 게임 서버 시스템의 통제 가능성을 융합한 시뮬레이션 프로젝트*

```mermaid
graph LR
    subgraph Client Layer
        Unity[Unity Client]
    end

    subgraph Physical World Engine
        CPP[C++ Game Server<br/>20Hz Lock-Free Loop<br/>Spatial Hash Grid]
    end

    subgraph Cognitive AI Engine
        CS[C# AI API Server<br/>Belief Decay & Mutation<br/>Dialogue Orchestration]
        LLM[(Google Gemini API)]
    end

    Unity <-->|TCP / Protobuf| CPP
    CPP <-->|gRPC Bidirectional Streaming| CS
    CS <-->|HTTPS REST| LLM
```

- **Architecture**: C++ 게임 서버와 C# AI 인지 백엔드 서버 간의 **고성능 gRPC 양방향 비동기 스트리밍 파이프라인** 구축.
- **C++ Game Server**: 데이터 레이스를 방지하고 임계 구역(Critical Section) 대기 시간을 최소화하는 **더블 버퍼드 락-스왑(Lock-Swap) 기반 3-스레드 Proactor 모델** 및 공간 해시 그리드(Spatial Hash Grid) 기반의 틱 동기화 시뮬레이션 엔진 구현.
- **C# AI Engine**: 단기/중기/장기(Core) 메모리를 관리하는 **통합 믿음(Belief) 엔진** 설계. 에이전트 간의 정보 전파와 시간 경과에 따른 쇠퇴(Decay) 및 와전(Mutation)을 시뮬레이션화.
- **Behavior & Survival**: 물리적 생존 본능(허기/피로)이 발생하면 AI 대뇌의 일정을 즉시 인터럽트하는 생존 오버라이드(Survival Override) 및 과거 트라우마 기억을 바탕으로 공격성을 동적으로 제어하는 위협 억제 파이프라인(Threat Inhibition) 구축.

---

### GRC (Generative AI Roleplay Chat)
*Google Gemini API 기반의 고몰입도 롤플레잉 및 서사 창작용 WPF 데스크톱 어플리케이션*

- **Memory Architecture**: 컨텍스트 윈도우 한계를 극복하기 위해 대화 기록을 계층화한 **3단계 메모리 압축 파이프라인**(Raw History -> Chapter Plot -> Chronicle) 설계.
- **TRPG Orchestration**: 에이전트 기반 자율 TRPG 세션 빌더와 프롬프트 오류 방지를 위한 실시간 자율 감사관(Auditor) 루프 내장.
- **Multimodal Integration**: Gemini 멀티모달 오디오 스트리밍 및 사용자 감정 가중치를 이용한 동적 분기형 TTS 연출 처리.

---

## Connect with me

- **Email**: adg01008@naver.com

