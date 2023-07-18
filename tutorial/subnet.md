# 다른 네트워크(Subnet) 서버 환경 구성

## 개요

IP 대역이 다른 두 개의 Subnet에 각각 Server를 생성하고, Server 간에 통신이 가능하도록 해보겠습니다.\
외부와 연결되는 서버(DMZ)와 내부에 격리된 서버(Legacy) 구성할 때 활용할 수 있는 사례입니다.

#### 네트워크 구성도

<figure><img src="../.gitbook/assets/image (102).png" alt=""><figcaption></figcaption></figure>



## 절차

1. [Project를 생성합니다.](../common/project.md#project-4)
2. [Project 하위에 VPC를 생성합니다.](../network/vpc.md#vpc-1)
   * 예시) VPC IP 주소 범위: 10.201.0.0/16
3. [VPC 하위에 Subnet을 두 개 생성합니다.](../network/subnet.md#subnet-1)
   * 예시) Subnet-WEB IP 주소 범위: 10.201.1.1/24
   * 예시) Subnet-WAS IP 주소 범위: 10.201.2.1/24&#x20;
4. [Subnet Routing을 설정](../network/subnet-routing.md#subnet-routing-1)하여 두 개 Subnet이 통신 가능하도록 합니다.
   * 예시) 출발지: Subnet-WEB, 목적지: Subnet-WAS
5. 각각의 [Subnet 하위에 Server를 생성합니다.](../compute/server.md#server-2)
   * 예시) Subnet-WEB의 Server: DMZ-WEB
   * 예시) Subnet-WAS의 Server: WAS01
6. 각 서버의 [Terminal](../compute/server.md#server-terminal)에 접속하여 Routing 설정한 방향으로 통신이 가능한지 확인합니다.

