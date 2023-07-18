# Subnet

## 개요

#### 소개

Subnet 은 [VPC](vic.md) 내 세분화된 네트워크 영역을 의미합니다. 또한 Subnet 은 VPC IP 주소 범위 내 세분화된 IP 주소 범위를 갖습니다. Subnet 은 독립된 네트워크 영역으로 같은 VPC 내 존재하더라도 기본적으로 통신이 불가능합니다. VPC 내 Subnet 간 통신을 위해서 [Subnet Routing](routing/subnet-routing.md) 기능이 필요합니다.



## 사용 가이드

#### Subnet 목록 조회

왼쪽 메뉴에서 Network > Subnet 을 클릭하여 Subnet 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (207).png" alt=""><figcaption></figcaption></figure>



#### Subnet 생성

Subnet 생성은 VPC 내 Subnet 을 생성하는 기능입니다. VPC 에 대한 접근 권한이 필요하며, VPC 내 Subnet 간 IP 주소 범위는 겹칠 수 없습니다. Subnet은 VPC 당 최대 15개 생성 가능합니다.

{% tabs %}
{% tab title="1. 생성 화면 이동" %}
* 왼쪽 메뉴에서 Network > Subnet 을 선택합니다.
* Subnet 목록 화면이 나타나면 상단 메뉴 중 생성 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (146).png" alt=""><figcaption></figcaption></figure>

* Subnet 생성을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. Subnet 생성" %}
**필수 입력 사항**

* Subnet 이름 : 생성될 Subnet 의 이름입니다. 3byte\~20byte 이내로 영문 및 숫자, '-' 만 입력 가능합니다.
* VPC : 생성될 Subnet 이 위치할 VPC 입니다.
* Subnet 주소 : 생성될 Subnet 의 IP 주소 범위 입니다. 선택한 VPC 의 IP 주소 범위 내에서 입력 가능합니다.
* Security Group : 생성될 Subnet 에 적용될 Security Group입니다. 이 Subnet 을 통해 통신하는 Server 는 해당 보안 그룹이 적용됩니다.

선택 입력 사항

* 설명 : Subnet 에 대한 상세한 설명입니다.

<figure><img src="../.gitbook/assets/image (97).png" alt=""><figcaption></figcaption></figure>

* 팝업 창 우측 하단의 생성 버튼을 클릭합니다.
* 팝업 창이 닫히고, Subnet 목록 화면에 생성한 Subnet이 추가된 것이 확인됩니다.
{% endtab %}
{% endtabs %}

{% hint style="info" %}
참조

Subnet 생성 시, Fabric > [PathGroup](../fabric/pathgroup.md) 에 등록된 Subnet 유형의 PathGroup 정보가 사용됩니다. Subnet 유형의 PathGroup 없다면 Subnet을 생성할 수 없습니다.

만약 Subnet 유형의 PathGroup 이 두 개 이상이라면 먼저 생성된 PathGroup 정보가 우선 적용됩니다.
{% endhint %}



#### Subnet 수정

Subnet 정보를 수정하는 기능입니다. VPC, Subnet 이름, Subnet 주소는 수정이 불가능합니다.

{% tabs %}
{% tab title="1. 수정 화면 이동" %}
* 왼쪽 메뉴에서 Network > Subnet 을 선택합니다.
* Subnet 목록 화면이 나타나면 수정하려는 Subnet을 선택한 후 상단의 수정 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (149).png" alt=""><figcaption></figcaption></figure>

* Subnet 수정을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. Subnet 수정" %}
**필수 입력 사항**

* Security Group : 생성될 Subnet 에 적용될 보안 그룹입니다. 이 Subnet 을 통해 통신하는 Server 는 해당 보안 그룹이 적용됩니다.

선택 입력 사항

* 설명 : Subnet 에 대한 상세한 설명입니다.

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

* 수정이 끝나면 팝업 창 우측 하단의 수정 버튼을 클릭합니다.
* 팝업 창이 닫히고, Subnet 목록 화면에 수정한 내용이 반영되어 보입니다.
{% endtab %}
{% endtabs %}



#### Subnet 삭제

Subnet 삭제는 VPC 내 Subnet 을 삭제하는 기능입니다. 삭제 대상 Subnet 을 이용 중인 Server 가 없어야 Subnet 삭제가 가능합니다.

{% tabs %}
{% tab title="1. 삭제 화면 이동" %}
* 왼쪽 메뉴에서 Network > Subnet 을 선택합니다.
* Subnet 목록 화면이 나타나면 삭제하려는 Subnet을 선택한 후 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>

* Subnet 삭제를 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. Subnet 삭제" %}
* 팝업 창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (76).png" alt=""><figcaption></figcaption></figure>

* 삭제 팝업 창이 닫히고, Subnet 목록에서 삭제되었는지 확인합니다.
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
주의

Sunbet을 삭제하면 삭제 대상 Subnet이 포함된 하위 Routing 목록도 함께 삭제됩니다.

* Subnet Routing
* VPC Routing
* External Gateway 연결
{% endhint %}



## FAQ

> **Q. Subnet 생성이 되지 않습니다.**
>
> A. [Subnet 생성](subnet.md#subnet) 을 참고해주시기 바랍니다. 만약 해결 되지 않는다면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.

> **Q. Subnet 삭제가 되지 않습니다.**
>
> A. [Subnet 삭제](subnet.md#subnet-2) 를 참고해주시기 바랍니다. 만약 해결 되지 않는다면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.

> **Q. Subnet 는 몇 개까지 생생 가능한가요?**
>
> A. Subnet 는 VPC 당 최대 15개 생성 가능합니다.
