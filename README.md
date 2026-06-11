## Hi there 👋

<a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fjin20203458&count_bg=%233DC84A&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false"/></a>

[![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=jin20203458)](https://github.com/jin20203458/github-readme-stats)
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=jin20203458&layout=compact)](https://github.com/jin20203458/github-readme-stats)

[![Solved.ac Profile](http://mazassumnida.wtf/api/v2/generate_badge?boj=naneunmuneo)](https://solved.ac/naneunmuneo/)
[![Solved.ac Profile](https://mazandi.herokuapp.com/api?handle=naneunmuneo&theme=warm)](https://solved.ac/naneunmuneo)

>  **LLVM/Clang 기반 소프트웨어 테스트 솔루션 <img width="252" height="61" alt="image" src="https://github.com/user-attachments/assets/030873a4-f3eb-487e-899d-69b512ffb6d9" />
의 메인 소프트웨어 엔지니어**로서, 저수준 컴파일러 인프라 가공부터 비동기 데스크톱 어플리케이션 아키텍처 및 AI 연동 파이프라인까지 풀스택으로 설계하고 개발합니다.

<!--
**jin20203458/jin20203458** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

---

## Tech Stacks & Architecture

###  Core Languages & Frameworks
- **C++**: Low-Level System Programming / Custom Memory Pool 구현 및 메모리 최적화
- **C# / .NET**: WPF 기반 비동기 멀티스레딩 아키텍처 / UI Thread Freezing 방어 및 최적화

###  LLM & AI 응용 엔지니어링 (AI 파이프라인 제어)
- **Context 오케스트레이션**: LLM 어텐션 희석 방지를 위한 **Context Pruning(맥락 정제)** 파이프라인 설계
- **비용·레이턴시 최적화**: Gemini Flash 등 경량 모델 가성비 극대화 및 **Prefetch 기반 비동기 백그라운드 처리**
- **Defensive Guardrail**: 생성형 모델의 출력 예외 및 포맷 파괴(**Silent Failure**) 방어 파서 구축
- **자율형 에이전트 워크플로우**: **Human-In-The-Loop(유저 승인)** 기반의 [계획-검증-연동] 생태계 설계

###  System & Compiler Infrastructure
- **컴파일러 인프라**: **LLVM/Clang AST Core** 가공 및 Custom 분석 패스(Pass) 설계
- **프로그램 정적 분석**: Lexer, AST Matcher/Visitor, CFG, **Clang Static Analyzer(기호 실행/Symbolic Execution)** 기반 다중 레이어 보안 진단 툴 마감 경험
- **네트워크 & 동시성**: Winsock/IOCP 아키텍처 이해 / 대규모 스트리밍 환경에서의 프로세스 격리(Process Isolation) 및 무상태(Stateless) 처리

---

##  Featured Projects

- **ARQA Static (LLVM-Based Static Analysis Tool)** `Main Engineer`
  - 대규모 상용 C/C++ 소스코드 취약점 진단 및 LLM 연동 자가 치유(Self-Healing) 정적 분석 플랫폼
  - **역할 및 기여:** 
    - WPF 기반 클라이언트의 비동기 아키텍처 및 다국어화(Localization) 시스템 설계
    - LLVM/Clang AST 정적 분석 엔진 연동 모듈 및 분석 프로세스 백그라운드 처리 최적화 주도

- **GRC (Git Repository Chat)**
  - 소스코드 레포지토리 맥락 기반 실시간 AI 페르소나 런타임 추론 엔진 및 자율 콘텐츠 저작 에이전트 시스템
