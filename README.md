# What is autofortivpn
- **fortivpn** 연결 자동화를 위해서, **openfortivpn** 기반의 오픈소스인 **empatpuluh**에 기능을 추가한 자동화 툴
- 백그라운드 실행, 실행 상태 확인 등...


# How to setup
1. `autofortivpn` 레포지토리를 클론받는다.
2. 레포지토리 루트 경로에서 `sh setup` 커맨드를 실행한다.
3. **vpn username**, **vpn password**, **email account**, **2fa app password**를 차례로 입력한다.


# How to use
- `runvpn` : vpn 실행
- `checkvpn` : vpn 실행 여부 확인
  - 실행중이면 `VPN ON`, 그렇지 않으면 `VPN OFF` 출력
- `killvpn` : vpn 종료