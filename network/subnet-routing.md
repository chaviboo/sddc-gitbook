# Subnet Routing

## 개요

#### 소개

[Subnet](subnet.md) 은 독립된 네트워크 공간으로 동일한 VPC 내에 존재하더라도 서로 통신이 불가능하므로, 동일한 VPC 내 Subnet 간 통신을 가능하게 하려면 Subnet Routing을 생성해야 합니다. &#x20;

Subnet Routing 은 단방향 통신을 지원하며 '출발지 Subnet' -> '목적지 Subnet' 방향으로 통신 요청이 가능합니다.

Subnet 간 통신에 방화벽, 로드밸런서 등 네트워크 기능을 적용하려면 [PBR(Policy-Based-Redirect) 연결](subnet-routing.md#pbr)을 통해 Service Graph를 추가해야 합니다.



## 사용 가이드

#### Subnet Routing 목록 조회

왼쪽 메뉴에서 Network > Routing > Subnet Routing 을 클릭하여 Subnet Routing 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>



#### Subnet Routing 생성

Subnet Routing 생성은 한 VPC 내 Subnet 사이에 단방향 통신 관계를 생성하는 기능입니다. Subnet Routing을 생성하기 위해선 한 VPC 내 2개 이상의 Subnet 이 필요하며, Subnet은 최대 1개의 Subnet Routing 에 대해 '출발지 Subnet' 으로 등록될 수 있습니다.

{% tabs %}
{% tab title="1. 생성 화면 이동" %}
* 왼쪽 메뉴에서 Network > Routing > Subnet Routing 을 선택합니다.
* Subnet Routing 목록이 나타나면 상단 메뉴 중 생성 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (122).png" alt=""><figcaption></figcaption></figure>

* Subnet Routing 생성을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. Subnet Routing 생성" %}
**필수 입력 사항**

* Subnet Routing 이름 : 생성될 Subnet Routing 의 이름입니다.
* VPC : '출발지/목적지 Subnet' 이 존재하는 VPC 입니다.
* 출발지 Subnet : 단방향 통신 요청의 출발지가 되는 Subnet 입니다.
* 목적지 Subnet : 단방향 통신 요청의 목적지가 되는 Subnet로, 복수 개 선택이 가능합니다.

선택 입력 사항

* 설명 : Subnet Routing 에 대한 상세한 설명입니다.

<figure><img src="../.gitbook/assets/image (214).png" alt=""><figcaption></figcaption></figure>

* 팝업 창 우측 하단의 생성 버튼을 클릭합니다.
* 팝업 창이 닫히고, Subnet Routing 목록 화면에 생성한 Subnet Routing이 추가된 것이 확인됩니다.
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
주의

* Subnet Routing 생성 후 '출발지 Subnet' 은 수정이 불가능합니다.
{% endhint %}

#### Subnet Routing 수정

Subnet Routing 정보를 수정하는 기능입니다. Subnet Routing 이름, VPC, 출발지 Subnet은 수정이 불가능합니다.

{% tabs %}
{% tab title="1. 수정 화면 이동" %}
* 왼쪽 메뉴에서 Network > Routing > Subnet Routing 을 선택합니다.
* Subnet Routing 목록 화면이 나타나면 수정하려는 Subnet Routing을 선택한 다음, 상단의 수정 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

* Subnet Routing 수정 팝업 창이 화면에 나타납니다.


{% endtab %}

{% tab title="2. Subnet Routing 수정" %}
* Subnet Routing 수정 팝업 창에서는 설명 항목만 수정이 가능합니다.
* 설명 수정 후, 팝업 창 우측 하단의 수정 버튼을 클릭 합니다.
* 팝업 창이 닫히고, 수정 사항이 목록에 반영되어 조회됩니다.

<figure><img src="../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>



* Subnet Routing에 등록된 목적지 Subnet을 수정하고자 할 경우, 팝업창 좌측 하단의 Routing 관리 버튼을 클릭합니다.
* Routing 관리 팝업 창이 나타납니다.

<figure><img src="../.gitbook/assets/image (163).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="3. Routing 관리" %}
Subnet Routing에 등록된 목적지 Subnet을 추가, 삭제할 수 있습니다.

**목적지 Subnet 추가**

* 목적지 Subnet 콤보박스에서 원하는 Subnet을 선택한 다음 추가 버튼을 클릭합니다.
* 목적지 Subnet 테이블에 Subnet이 추가됩니다.

**목적지 Subnet 삭제**

* 목적지 Subnet 테이블에서 삭제하고자 하는 Subnet 행의 삭제 버튼을 클릭합니다.
* 목적지 Subnet 목록 테이블에서 Subnet이 삭제됩니다.

{% hint style="info" %}
참고

'목적지 Subnet' 추가나 삭제 시 Subnet Routing에 즉시 반영됩니다.
{% endhint %}

<figure><img src="../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure>

* 목적지 Subnet 목록 수정 후 Routing 관리 팝업 창 우측 하단의 확인 버튼을 눌러 팝업 창을 닫습니다.
{% endtab %}
{% endtabs %}



#### Subnet Routing 삭제

{% tabs %}
{% tab title="1. 삭제 화면 이동" %}
* 왼쪽 메뉴에서 Network > Routing > Subnet Routing 을 선택합니다.
* Subnet Routing 목록 화면이 나타나면 삭제하려는 Subnet Routing을 선택한 다음, 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="2. Subnet Routing 삭제" %}
* 팝업 창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>

* 삭제 팝업 창이 닫히고, Subnet Routing 목록에서 삭제되었는지 확인합니다.
{% endtab %}
{% endtabs %}



#### PBR 연결

Routing 에 [Service Graph](../fabric/service-graph.md) 를 연결하는 기능입니다. 이를 통해 Routing 에 따라 Traffic 이 이동하는 과정에 연결한 Service Graph 기능을 적용할 수 있습니다. 사전에 등록된 Service Graph 가 필요합니다.

{% tabs %}
{% tab title="1. PBR 연결 화면 이동 " %}
* 왼쪽 메뉴에서 Network > Routing > Subnet Routing을 선택합니다.
* Subnet Routing 목록 화면이 나타나면 Subnet Routing을 선택한 다음, PBR 연결 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (216).png" alt=""><figcaption></figcaption></figure>

* PBR 연결을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. PBR 연결" %}
**필수 입력 사항**

* Service Graph : 방화벽, 로드밸런서 등과 같은 네트워크 기능입니다.

<figure><img src="../.gitbook/assets/image (147).png" alt=""><figcaption></figcaption></figure>

* Service Graph 선택 후, 팝업 창 우측 하단의 연결 버튼을 클릭합니다.
* 팝업 창이 닫히고, Subnet Routing 목록 화면에서 PBR 연결 상태를 확인합니다.
{% endtab %}
{% endtabs %}



#### PBR 해제

{% tabs %}
{% tab title="1. PBR 해제 화면 이동" %}
* 왼쪽 메뉴에서 Network > Routing > Subnet Routing을 선택합니다.
* Subnet Routing 목록 화면이 나타나면 Subnet Routing을 선택한 다음, PBR 해제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

* PBR 해제를 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. PBR 해제" %}
* 팝업 창 우측의 해제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

* 팝업 창이 닫히고, Subnet Routing 목록에서 PBR이 해제되었음을 확인합니다.
{% endtab %}
{% endtabs %}



## FAQ

> **Q. Subnet Routing 생성이 되지 않습니다.**
>
> A. [Subnet Routing 생성](subnet-routing.md#subnet-routing) 을 참고해주시기 바랍니다. 만약 해결 되지 않는다면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.

> **Q. Subnet Routing의 VPC 또는 출발지 Subnet을 수정하고 싶습니다.**
>
> A. Subnet Routing의 VPC와 출발지 Subnet은 수정이 불가능합니다. 수정이 필요한 경우, Subnet Routing을 신규로 생성해야 합니다.

> **Q. PBR 연결이 되지 않습니다.**
>
> A. [PBR 연결](subnet-routing.md#pbr) 을 참고해주시기 바랍니다. 만약 해결 되지 않는다면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.
