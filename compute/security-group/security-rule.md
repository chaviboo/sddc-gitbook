# Security Rule

## 개요

#### 소개

Security Rule은 서버에서 발생하는 송신(Egress)/수신(Ingress) 트래픽을 제어함으로써 서버를 안전하게 보호할 수 있습니다. Security Rule은 stateful 방식으로 동작하며 규칙이 존재할 경우 허용하는 white list 방식인  positive security model 입니다.

#### Security Rule 설정

방향, IP 프로토콜, Port, Ether 범위, Remote (원격) 로 보안 정책을 설정합니다.&#x20;

#### Security Rule 예시

TCP 프로토콜로 IP가 192.168.1.56에서 서버로 들어오는 트래픽을 허용하는 규칙입니다.

| 방향 | IP 프로토콜 | Port | Ether 범위 | Remote (원격)     |
| -- | ------- | ---- | -------- | --------------- |
| 수신 | TCP     | 전체   | IPv4     | 192.168.1.56/32 |

전체 프로토콜로 0.0.0.0/0 으로 서버에서 나가는 트래픽을 허용하는 규칙입니다.

| 방향 | IP 프로토콜 | Port | Ether 범위 | Remote (원격) |
| -- | ------- | ---- | -------- | ----------- |
| 송신 | 전체      | 전체   | IPv4     | 0.0.0.0/0   |

ICMP 프로토콜로 192.168.1.0/24 에서 서버로 들어오는 트래픽을 허용하는 규칙입니다.

| 방향 | IP 프로토콜 | 타입 / 코드 | Ether 범위 | Remote (원격)    |
| -- | ------- | ------- | -------- | -------------- |
| 수신 | ICMP    | 0 / 8   | IPv4     | 192.168.1.0/24 |

#### Server를 위한 필수적인 Security Rule

서버 통신을 위한 필수적인 Security Rule들이 다음과 같이 4건이 존재합니다.&#x20;

<table><thead><tr><th width="151">방향</th><th width="153">IP 프로토콜</th><th width="104">Port</th><th width="111">Ether 범위</th><th>Remote IP</th></tr></thead><tbody><tr><td>송신</td><td>TCP</td><td>80</td><td>IPv4</td><td>169.254.169.254/32</td></tr><tr><td>송신</td><td>UDP</td><td>67</td><td>IPv4</td><td>0.0.0.0/0</td></tr><tr><td>송신</td><td>UDP</td><td>68</td><td>IPv4</td><td>0.0.0.0/0</td></tr><tr><td>송신</td><td>UDP</td><td>53</td><td>IPv4</td><td>DNS server address</td></tr></tbody></table>

* 송신 + TCP + 80 + IPv4 + 169.254.169.254/32 규칙은 Server에 메타 데이터를 제공하기 위한 규칙입니다.
* 송신 + UDP + (67, 68) + IPv4 + 0.0.0.0/0 규칙은 DHCP 서버와 통신하기 위한 규칙으로 Server가 IP를 할당받기위해 필요한 규칙입니다.
* 송신 + UDP + 53 + IPv4 + {DNS server address}는 DNS 서버와 통신하기 위한 규칙입니다.                   예를 들면, Google의 DNS 서버 주소가 8.8.8.8/32 이므로 송신 + UDP + 53 + IPv4 + 8.8.8.8/32 규칙이 필요합니다.

{% hint style="danger" %}
경고

위와 같이 필수적인 규칙 4건이 존재하지 않을 때, 서버 통신이 오동작 할 수 있으므로 주의해주시길 바랍니다.
{% endhint %}



## 사용 가이드

#### Security Rule 목록 조회

{% tabs %}
{% tab title="1. Rule 관리 화면 이동" %}
* 왼쪽 메뉴에서 Compute > Security Group을 선택합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>

* Security Group 목록 화면이 나타나면 수정하려는 Security Group을 선택한 다음, 상단의 Security Rule 관리 버튼을 클릭합니다.
{% endtab %}

{% tab title="2. Security Rule 조회" %}
* Security Rule 관리 팝업 창이 열리면, 해당 Security Group에 등록된 Security Rule 리스트를 조회합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>
{% endtab %}
{% endtabs %}



#### Security Rule 생성

Security Rule을 생성하려면 기본적으로 사전에 준비되어할 자원들이 있습니다. 기본적으로 생성 되어야하는 자원은 Security Group이 있으며 자세한 내용은 [Security Group](./)을 참고합니다.

{% tabs %}
{% tab title="1. Rule 관리 화면 이동" %}
* [Security Rule 목록 조회](security-rule.md#security-rule-2) 가이드에 따라 Security Rule 관리 팝업창을 실행합니다.
{% endtab %}

{% tab title="2. Security Rule 생성" %}
* 방향, IP 프로토콜, Port, Ether 범위, Remote 를 입력합니다.
* 추가버튼을 클릭하면, 해당 Security Rule이 추가되어 테이블에 반영됩니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>
{% endtab %}
{% endtabs %}



#### Security Rule 수정

{% tabs %}
{% tab title="1. Rule 관리 화면 이동" %}
* [Security Rule 목록 조회](security-rule.md#security-rule-2) 가이드에 따라 Security Rule 관리 팝업창을 실행합니다.
{% endtab %}

{% tab title="2. Security Rule 수정" %}
* 원하는 Security Rule의 수정 버튼을 클릭합니다. 해당 테이블 행이 편집 가능 상태로 변경됩니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>

* 방향, IP 프로토콜, Port, Ether 범위, Remote (원격) 를 수정합니다.
* 아래 하단의 수정 버튼을 클릭하면 Security Rule 변경사항이 반영됩니다.
* 수정 사항을 반영하지 않을 경우, 아래 하단의 취소 버튼을 클릭하여 원래 데이터 상태로 되돌립니다.
{% endtab %}
{% endtabs %}



#### Security Rule 삭제

{% tabs %}
{% tab title="1. Rule 관리 화면 이동" %}
* [Security Rule 목록 조회](security-rule.md#security-rule-2) 가이드에 따라 Security Rule 관리 팝업창을 실행합니다.
{% endtab %}

{% tab title="2. Security Rule 삭제" %}
* 원하는 Security Rule의 삭제 버튼을 클릭합니다.
* 수정 버튼을 클릭해야만 해당 사항이 반영됩니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>
{% endtab %}
{% endtabs %}



## FAQ

> **Q. 프로토콜을 전체로 선택했을 때, Port 범위를 지정할 수 있나요?**
>
> 아니요. 프로토콜을 전체로 선택했을 때, Port 범위는 전체로 지정되며 따로 지정할 수 없습니다.

> **Q. Security Group을 생성할 때, 자동으로 생성되는 기본 Security Rule을 수정, 삭제할 수 있나요?**
>
> 네. Security Group 생성시에는 변경할 수 없지만, 생성 이후에는 기본 Security Rule들을 수정, 삭제 할 수 있습니다.



