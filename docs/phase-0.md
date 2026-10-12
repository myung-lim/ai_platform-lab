# Phase 0 학습 노트

## 한 일
- WSL2 Ubuntu 24.04 + .wslconfig (memory 20GB, mirrored 네트워크)
- Docker Engine 확인 (hello-world)
- VSCode WSL 연결
- GitHub Deploy key + SSH 별칭(github-ai-platform) + clone

## 배운 것 (내 말로 정리)
- 공개키/개인키는 각각 어디에 두는가:
   - 공개키: 접속할 상대(GitHub, 서버)에 등록
   - 개인키: 내 컴퓨터(~/.ssh)에만 보관, 절대 외부 유출 금지
- Deploy key와 계정 SSH key의 차이:
   - Deploy key: 저장소 하나에만 등록, 그 저장소만 접근 (쓰기 권한은 선택)
   - 계정 SSH key: GitHub 계정에 등록, 내가 접근 가능한 모든 저장소 사용
- known_hosts의 역할:
   - 접속했던 서버의 지문 목록. 다음 접속 때 같은 서버인지 확인해 가짜 서버를 막음
- .wslconfig / wsl.conf / ~/.ssh/config 차이:
   - .wslconfig (Windows 사용자 폴더): WSL 전체에 적용, 메모리·CPU·네트워크 방식
   - wsl.conf (Ubuntu 안 /etc): 이 Ubuntu 배포판만 적용, systemd 켜기·기본 사용자
   - ~/.ssh/config (Ubuntu 안): 이 사용자의 SSH만 적용, GitHub 별칭·사용할 키
- 커밋 작성자 이메일이 다른 계정으로 표시된 이유:
   - GitHub는 push한 사람이 아니라 커밋에 적힌 이메일로 작성자를 표시함
   - noreply 주소의 숫자ID가 다른 사용자의 고유번호여서 그 사람으로 표시됨
