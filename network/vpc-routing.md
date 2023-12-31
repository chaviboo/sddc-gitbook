# VPC Peering

## 개요

#### 소개

동일한 Project 내 서로 다른 VPC 하위에 있는 Subnet 간 통신을 위한 연결 기능입니다. [VPC](vpc.md) 는 독립된 네트워크 공간으로 동일한 Project 내에 존재하더라도 서로 통신이 불가능합니다. VPC Routing 은 단방향 통신을 지원하며 '출발지 Subnet' -> '목적지 Subnet' 방향으로 통신 요청이 가능합니다.

[PBR(Policy-Based-Redirect) 연결](vpc-routing.md#pbr)을 통해 VPC Routing 에 Service Graph 를 연결하여 VPC간 통신에 방화벽, 로드밸런서 등 네트워크 기능을 적용할 수 있습니다.



## 사용 가이드

#### VPC Routing 목록 조회

왼쪽 메뉴에서 Network > Routing > VPC Routing 을 클릭하여 VPC Routing 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>



#### VPC Routing 생성

VPC Routing 생성은 서로 다른 VPC 내 Subnet 사이에 단방향 통신 관계를 생성하는 기능입니다. VPC Routing을 생성하기 위해선 2개 이상의 VPC 가 필요하며, 각 VPC 내 1개 이상의 Subnet 이 필요합니다. Subnet은 최대 1개의 VPC Routing 에 대해 '출발지 Subnet' 으로 등록될 수 있습니다.

{% tabs %}
{% tab title="1. 생성 화면 이동" %}
* 왼쪽 메뉴에서 Network > Routing > VPC Routing 을 선택합니다.
* VPC Routing 목록이 나타나면 상단 메뉴 중 생성 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (169).png" alt=""><figcaption></figcaption></figure>

* &#x20;VPC Routing 생성을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. VPC Routing 생성" %}
**필수 입력 사항**

* VPC Routing 이름 : 생성될 VPC Routing 의 이름입니다.
* 출발지 Subnet : 단방향 통신 요청의 출발지가 되는 Subnet 입니다.
* 목적지 Subnet : 단방향 통신 요청의 목적지가 되는 Subnet 입니다. 목록으로 관리됩니다.

선택 입력 사항

* 설명 : VPC Routing 에 대한 상세한 설명입니다.

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

* 팝업 창 우측 하단의 생성 버튼을 클릭합니다.
* 팝업 창이 닫히고, VPC Routing 목록 화면에 생성한 VPC Routing이 추가된 것을 확인합니다.
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
주의

* VPC Routing 생성 후 '출발지 Subnet' 은 수정이 불가능합니다.
{% endhint %}



#### VPC Routing 수정

VPC Routing 정보를 수정하는 기능입니다. VPC Routing 이름과 출발지 Subnet은 수정이 불가능합니다.

{% tabs %}
{% tab title="1. 수정 화면 이동" %}
* 왼쪽 메뉴에서 Network > Routing > VPC Routing 을 선택합니다.
* VPC Routing 목록 화면이 나타나면 수정하려는 VPC Routing을 선택한 다음, 상단의 수정 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (171).png" alt=""><figcaption></figcaption></figure>

* VPC Routing 수정 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. VPC Routing 수정" %}
* VPC Routing 수정 팝업 창에서는 설명 항목만 수정이 가능합니다.
* 설명 수정 후, 팝업 창 우측 하단의 수정 버튼을 클릭 합니다.
* 팝업 창이 닫히고, 수정 사항이 목록에 반영되어 조회됩니다.

<figure><img src="../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure>



* VPC Routing에 등록된 목적지 Subnet을 수정하고자 할 경우, 팝업창 좌측 하단의 Routing 관리 버튼을 클릭합니다.
* Routing 관리 팝업 창이 나타납니다.

<figure><img src="../.gitbook/assets/image (121).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="3. Routing 관리" %}
VPC Routing에 등록된 목적지 Subnet을 추가, 삭제할 수 있습니다.

**목적지 Subnet 추가**

* 목적지 Subnet 콤보박스에서 원하는 Subnet을 선택한 다음 추가 버튼을 클릭합니다.
* 목적지 Subnet 테이블에 Subnet이 추가됩니다.

**목적지 Subnet 삭제**

* 목적지 Subnet 테이블에서 삭제하고자 하는 Subnet 행의 삭제 버튼을 클릭합니다.
* 목적지 Subnet 목록 테이블에서 Subnet이 삭제됩니다.

{% hint style="info" %}
참고

'목적지 Subnet' 추가나 삭제 시 VPC Routing에 즉시 반영됩니다.
{% endhint %}

<figure><img src="../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

* 목적지 Subnet 목록 수정 후 Routing 관리 팝업 창 우측 하단의 확인 버튼을 눌러 팝업 창을 닫습니다.
{% endtab %}
{% endtabs %}



#### VPC Routing 삭제

{% tabs %}
{% tab title="1. 삭제 화면 이동" %}
* 왼쪽 메뉴에서 Network > Routing > VPC Routing 을 선택합니다.
* VPC Routing 목록 화면이 나타나면 삭제하려는 VPC Routing을 선택한 다음, 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="2. VPC Routing 삭제" %}
* 팝업 창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

* 삭제 팝업 창이 닫히고, Subnet Routing 목록에서 삭제되었는지 확인합니다.
{% endtab %}
{% endtabs %}



#### PBR 연결

Routing 에 [Service Graph](../vnf-mgmt/vnf/service-graph.md) 를 연결하는 기능입니다. 이를 통해 Routing 에 따라 Traffic 이 이동하는 과정에 연결한 Service Graph 기능을 적용할 수 있습니다. 사전에 등록된 Service Graph 가 필요합니다.

{% tabs %}
{% tab title="1. PBR 연결 화면 이동 " %}
* 왼쪽 메뉴에서 Network > Routing > VPC Routing을 선택합니다.
* VPC Routing 목록 화면이 나타나면 VPC Routing을 선택한 다음, PBR 연결 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (190).png" alt=""><figcaption></figcaption></figure>

* PBR 연결을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. PBR 연결" %}
**필수 입력 사항**

* Service Graph : 방화벽, 로드밸런서 등과 같은 네트워크 기능입니다.

<figure><img src="../.gitbook/assets/image (131).png" alt=""><figcaption></figcaption></figure>

* Service Graph 선택 후, 팝업 창 우측 하단의 연결 버튼을 클릭합니다.
* 팝업 창이 닫히고, VPC Routing 목록 화면에서 PBR 연결 상태를 확인합니다.
{% endtab %}
{% endtabs %}



#### PBR 해제

{% tabs %}
{% tab title="1. PBR 해제 화면 이동" %}
* 왼쪽 메뉴에서 Network > Routing > VPC Routing을 선택합니다.
* VPC Routing 목록 화면이 나타나면 VPC Routing을 선택한 다음, PBR 해제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (172).png" alt=""><figcaption></figcaption></figure>

* PBR 연결 해제를 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. PBR 해제" %}
* 팝업 창 우측 하단의 연결 해제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (158).png" alt=""><figcaption></figcaption></figure>

* 팝업 창이 닫히고, VPC Routing 목록 화면에서 PBR이 해제되었음을 확인합니다.
{% endtab %}
{% endtabs %}



## FAQ

> **Q. VPC Routing 생성이 되지 않습니다.**
>
> A. [VPC Routing 생성](vpc-routing.md#vpc-routing) 을 참고해주시기 바랍니다. 만약 해결 되지 않는다면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.

> **Q. VPC Routing의 출발지 Subnet을 수정하고 싶습니다.**
>
> A. VPC Routing의 출발지 Subnet은 수정이 불가능합니다. 수정이 필요한 경우, VPC Routing을 신규로 생성해야 합니다.

> **Q. PBR 연결이 되지 않습니다.**
>
> A. [PBR 연결](vpc-routing.md#pbr) 을 참고해주시기 바랍니다. 만약 해결 되지 않는다면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.
