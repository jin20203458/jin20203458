## Hi there 👋


[![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=jin20203458)](https://github.com/jin20203458/github-readme-stats)
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=jin20203458&layout=compact)](https://github.com/jin20203458/github-readme-stats)

[![Solved.ac Profile](http://mazassumnida.wtf/api/v2/generate_badge?boj=naneunmuneo)](https://solved.ac/naneunmuneo/)
<img width="252" height="61" alt="image" src="https://github.com/user-attachments/assets/030873a4-f3eb-487e-899d-69b512ffb6d9" />


>  **LLVM/Clang 기반  정적분석 소프트웨어 ARQA Static 메인 소프트웨어 엔지니어**로서, 저수준 컴파일러 인프라 가공부터 비동기 데스크톱 어플리케이션 아키텍처 및 AI 연동 파이프라인까지 풀스택으로 설계하고 개발합니다.

## Public

GRC (WPF & Gemini API 융합 프로젝트)
- LLM 컨텍스트 한계 및 Lost-in-the-Middle 문제 극복을 위한 3단계 요약식 계층 메모리 및 재귀 로어북 아키텍처 설계.
- 무거운 텍스트뷰 실시간 갱신 렉을 방지하는 비동기 스트리밍 채널 파이프라인 및 디스패처 스로틀링 구현.
- AI 에이전트의 6단계 규격 기획을 자가 검증하는 상태 기계 기반의 감사관(Self-Review) 자율 완주 루프 구축.

Project Mundus Vivens (AI NPC 자율 생태계 엔진)
- 플레이어 없이도 N명의 NPC들이 스스로 일과를 계획하고 조우하여 상호작용하는 3-Tier 분산 아키텍처(C++ 게임 서버 ↔ C# AI 엔진 ↔ Unity 렌더러) 설계.
- 대화 원본 로그에서 상태 변화 및 언급된 정보를 실시간 추출하여 호감도/신뢰도 관계 그래프에 비동기로 반영하는 LLM 후처리 파싱 파이프라인 구축.
- 정보가 대화를 거쳐 전파될 때 화자 간 신뢰도에 의해 주관적 확신도가 보정되고, 언어적 요약을 통해 왜곡이 누적되는 자연스러운 소문 변형(Gossip Mutation) 메커니즘 설계.
- 상용화를 위해 메인 대화 연기용(Gemini 3.5 Flash)과 요약/JSON 파싱용(Gemini 3.1 Flash-Lite)을 결합하여 호출당 비용을 극단적으로 제어하는 하이브리드 LLM 파이프라인 구현.
  * *Tip: NPC들의 성격 가치관(Persona)과 소문 전파 트리거를 JSON으로 선언적으로 빌드해 두고 시뮬레이터를 가동하면, 코드 수정 없이 월드 관찰자 모드에서 다양한 인간 사회 군상의 실험적 양상을 모니터링하기 좋습니다.*
 
MCP Context Feeder (AI 개발 생산성 향상 툴)
- 외부 AI 에이전트에게 복수의 참조 문서를 단일 통신으로 즉시 주입하기 위한 로컬 JSON-RPC / SSE 기반 서버 아키텍처 구축.
- 비개발자도 직관적으로 컨텍스트를 구성할 수 있도록 드래그 앤 드롭 및 실시간 예상 토큰 산출 파이프라인이 적용된 모던 UI 설계.

  * *Tip: 에이전트 지침 문서를 항목별 마크다운으로 구성해 두고 옵시디언(Obsidian)과 연동하여 관리하면, 프로젝트 도메인에 따라 프롬프트 지침을 편하게 스위칭할 수 있어 시너지가 매우 좋습니다.*
