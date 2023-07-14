# On-Premise와 연결 구성

## 개요

[다른 네트워크(Subnet) 서버 환경](subnet.md)에 추가적으로 SDDC Platform 밖의 네트워크 환경과 통신할 수 있는 연결을 구성해보도록 하겠습니다.

#### 네트워크 구성도

<figure><img src="../.gitbook/assets/image (142).png" alt=""><figcaption></figcaption></figure>



## 절차

1. [Project를 생성합니다.](../common/project.md#project-4)
2. [Project 하위에 VPC를 생성합니다.](../network/vpc.md#vpc-1)
   * 예시) VPC IP 주소 범위: 10.201.0.0/16
3. [VPC 하위에 Subnet을 두 개 생성합니다.](../network/subnet.md#subnet-1)
   * 예시) Subnet-WEB IP 주소 범위: 10.201.1.1/24
   * 예시) Subnet-WAS IP 주소 범위: 10.201.2.1/24&#x20;
4. [Subnet Routing을 설정](../network/subnet-routing.md#subnet-routing-1)하여 두 개 Subnet이 통신 가능하도록 합니다.
   * 예시) 출발지: Subnet-WEB, 목적지: Subnet-WAS
5. [External Gateway를 생성합니다.](../network/external-gateway-1.md#external-gateway-1)
   * External Gateway를 생성하려면 사전에 관리자에세 Gateway Info 설정을 요청해야 합니다.
   * 관리자가 설정한 Gateway Info 정보로 External Gateway를 생성합니다.
6. 외부와 통신을 하고자 하는 서버가 있는 Subnet에 [External Gateway를 연결](../network/external-gateway.md#external-gateway-1)합니다.
   * 예시) 연결한 Subnet: Subnet-WEB
7. 각각의 [Subnet 하위에 Server를 생성합니다.](../compute/server.md#server-2)
   * 예시) Subnet-WEB의 Server: DMZ-WEB
   * 예시) Subnet-WAS의 Server: WAS01
8. External Gateway를 연결한 Subnet에 생성한 Server [Terminal](../compute/server.md#server-terminal)에 접속하여 외부 네트워크에 존재하는 서버와 통신이 가능한지 확인합니다.

