# Network Interface

## 개요

#### 소개

Network Interface는 Server가 Subnet을 통해 내,외부로 통신할 수 있는 인터페이스입니다. Server는 Network Interface로 송수신되는 트래픽을 Security Group으로 네트워크 접근 제어를 관리할 수 있습니다.

#### DHCP Network Interface

Subnet을 생성하면 자동으로 생성되는 Network Interface입니다. 수정, 삭제할 수 없으며 Subnet을 삭제하면 자동으로 삭제됩니다.

## 사용가이드

#### Network Interface 목록 조회

왼쪽 메뉴에서 Network > Security Group 을 클릭하여 Security Group 목록을 조회합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>

#### Network Interface 생성

{% tabs %}
{% tab title="1. 생성화면 이동" %}
* 왼쪽 메뉴에서 Compute > Network Interface 을 선택합니다.
* Network Interface 목록이 나타나면 상단 메뉴 중 생성 버튼을 클릭합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>

* Network Interface 생성을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. Network Interface 생성" %}
**필수 입력 항목**

* &#x20;Network Interface 이름 : 이름은 영문과 숫자로 3Byte 이상 20Byte 이내로 작성해야하며 특수문자는 "-" 만 가능합니다

<mark style="color:blue;">**\[이미지 첨부]**</mark>



선택 입력 사항

* DHCP 사용/미사용
  * DHCP 사용을 선택할 경우 자동으로 고정 IP를 할당합니다.
  * DHCP 미사용을 선택할 경우, 사용자가 고정 IP를 지정하여 생성합니다.
{% endtab %}
{% endtabs %}

#### Network Interface 삭제

{% tabs %}
{% tab title="1. 삭제 화면 이동" %}
* 왼쪽 메뉴에서 Compute > Network Interface 을 선택합니다.
* &#x20;Network Interface 목록 화면이 나타나면 삭제하려는 Network Interface을 선택한 다음, 상단의 삭제 버튼을 클릭합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>

* &#x20;Network Interface 삭제을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. Network Interface 삭제" %}
* 팝업 창 우측 하단의 삭제 버튼을 클릭합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>

* 삭제 팝업 창이 닫히고, Network Interface 목록에서 삭제되었는지 확인합니다.
{% endtab %}
{% endtabs %}

#### Network Interface의 Security Group 적용

{% tabs %}
{% tab title="1. Security Group 적용 화면 이동" %}
* 왼쪽 메뉴에서 Compute >  Network Interface 을 선택합니다.
* Network Interface 목록 화면이 나타나면 수정하려는 Network Interface을 선택한 다음, 상단의 Security Group 수정 버튼을 클릭합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>

* Security Group 수정을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. Security Group 적용" %}
* Network Interface에 적용할 Security Group을 수정합니다.
* Security Group을 수정 후, 팝업 창 우측 하단의 수정 버튼을 클릭 합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>

* 팝업 창이 닫히고, 수정 사항이 목록에 반영되어 조회됩니다.
{% endtab %}
{% endtabs %}



## FAQ

> **Q. Security Group은 몇개 까지 적용이 가능한가요??**
>
> 최대 3개 까지 적용이 가능합니다.

