# Security Group

## 개요

#### 소개

Security Group은 서버 간 송수신을 제어하여 네트워크 접근 제어 및 관리를 할 수 있는  가상의 방화벽 서비스 입니다. Security Group은 [Security Rule](security-rule.md)들의 집합으로 서버에서 발생하는 인바운드/아웃바운드 트래픽을 Security Rule을 통해 허가 받지 않는 트래픽을 제어함으로써 서버를 안전하게 보호할 수 있습니다.&#x20;

#### 기본 Security Group

Project 생성 시 기본 Security Group이 1개 생성되어 제공됩니다. 기본 Security Group은  이름 수정, 삭제가 불가능 합니다. 기본 Security Group은 다음과 같은 Security Rule을 가지며 수정, 삭제가 가능합니다.

* 모든 송신(egress) 허용
* 모든 수신(ingress) 허용

#### 기본 Security Rule

추가적으로 Security Group을 생성할 때에는 다음과 같은 기본 Security Rule이 생성됩니다. 이때, 제공되는 기본 Security Rule은 Security Group 생성 시에는 수정, 삭제가 불가능하나 생성이 완료된 이후에는 수정, 삭제가 가능합니다.

* 모든 송신(egress) 허용



## 사용 가이드

#### Security Group 목록 조회

왼쪽 메뉴에서 Compute > Security Group 을 클릭하여 Security Group 목록을 조회합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>



#### Security Group 생성

{% tabs %}
{% tab title="1. 생성 화면 이동" %}
* 왼쪽 메뉴에서 Compute > Security Group 을 선택합니다.
* Security Group 목록이 나타나면 상단 메뉴 중 생성 버튼을 클릭합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>

* Security Group 생성을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. Security Group 생성" %}
**필수 입력 항목**

* Security Group 이름 : 이름은 영문과 숫자로 3Byte 이상 20Byte 이내로 작성해야하며 특수문자는 "-" 만 가능합니다

<mark style="color:blue;">**\[이미지 첨부]**</mark>

* 팝업 창 우측 하단의 생성 버튼을 클릭합니다.
* 팝업 창이 닫히고, Security Group 목록 화면에 생성한 Security Group이 추가된 것을 확인합니다.
{% endtab %}
{% endtabs %}



#### Security Group 수정

{% tabs %}
{% tab title="1. 수정 화면 이동" %}
* 왼쪽 메뉴에서 Compute > Security Group 을 선택합니다.
* Security Group 목록 화면이 나타나면 수정하려는 Security Group을 선택한 다음, 상단의 수정 버튼을 클릭합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>

* Security Group 수정을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. Security Group 수정" %}
* Security Group 이름을 수정합니다.
* Security Group 이름 수정 후, 팝업 창 우측 하단의 수정 버튼을 클릭 합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>

* 팝업 창이 닫히고, 수정 사항이 목록에 반영되어 조회됩니다.
{% endtab %}
{% endtabs %}



#### Security Group 삭제

{% tabs %}
{% tab title="1. 삭제 화면 이동" %}
* 왼쪽 메뉴에서 Compute > Security Group 을 선택합니다.
* Security Group 목록 화면이 나타나면 삭제하려는 Security Group을 선택한 다음, 상단의 삭제 버튼을 클릭합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>

* Security Group 삭제을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. Security Group 삭제" %}
* 팝업 창 우측 하단의 삭제 버튼을 클릭합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>

* 삭제 팝업 창이 닫히고, Security Group 목록에서 삭제되었는지 확인합니다.
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
주의

Network Interface에 할당된 Security Group은 삭제가 불가능 합니다. Network Interface에서 할당 해제 후 삭제하시길 바랍니다.

원격으로 사용 되고 있는 Security Group은 삭제가 불가능 합니다. Secuirty Rule을 제거한 이후, 삭제하시길 바랍니다.

기본 Security Group은 Server에 할당되어 있지 않아도 삭제가 불가능 합니다.
{% endhint %}



## FAQ

> **Q. Security Rule은 어떻게 설정해야하나요?**
>
> [Security Rule](security-rule.md)을 참조해 주세요.\
> \
> **Q. Security Group을 서버에 어떻게 적용하나요?**\
> [Network Interface](../network-interface.md)를 참조해 주세요
