# 단일 네트워크 서버 환경 구성

## 개요

외부와 격리된 단일 네트워크(Subnet)에 서로 통신이 가능한 두 개의 서버를 생성해보도록 합니다.

#### 네트워크 구성도

<figure><img src="../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>



## 절차

1. [Project를 생성합니다.](../tenant-member.md#project-4)
2. [Project 하위에 VPC를 생성합니다.](../network/vpc.md#vpc-1)
   * 예시) VPC IP 주소 범위: 10.220.0.0/16
3. [VPC 하위에 Subnet을 생성합니다.](../network/subnet.md#subnet-1)
   * 예시) Subnet-Local IP 주소 범위: 10.220.1.1/24
4. [Subnet 하위에 Server를 두 개 생성합니다.](../compute/server.md#server-2)
5. [Server Terminal에 접속하여 두 Server 간의 통신을 확인합니다.](../compute/server.md#server-terminal)

