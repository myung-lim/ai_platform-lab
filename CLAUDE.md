# ai_platform-lab
기업형 AI 플랫폼 학습 프로젝트 (M-API 프로젝트와 무관, ~/M-API는 수정하지 말 것)

- 실행 환경: Azure VM Ubuntu 24.04, 4 vCPU / 16GiB, GPU 없음
- LLM/임베딩: Mac mini의 Ollama (Tailscale로 접속, OpenAI 호환 API)
- 스택: FastAPI, PostgreSQL+pgvector, Keycloak, LangGraph, Docker Compose → 이후 k3s
- 폴더: backend/ ingest/ infra/compose/ infra/k8s/ docs/
- 비밀값은 .env에만 저장하고 커밋하지 않음
- 학습자는 초급: 명령어와 코드에 짧은 설명을 붙여줄 것
