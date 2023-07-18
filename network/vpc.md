# VPC

## 개요

#### 소개

VPC(Virtual Private Cloud)는 논리적으로 격리된 가상의 네트워크에서 SDDC Platform 리소스를 운영할 수 있는 기능을 제공합니다. VPC 는 Project 하위에 생성되며, 최대 3개 까지 생성 가능합니다. 동일한 Project 내 VPC 간 통신을 하기 위해선 [VPC Routing](vpc-routing.md) 이 필요합니다. 각 VPC 하위에 독립된 네트워크인 [Subnet](subnet.md)을 생성하여 IT 인프라를 안전하게 구축하고 간편하게 관리할 수 있습니다.&#x20;



## 사용 가이드

#### VPC 목록 조회

왼쪽 메뉴에서 Network > VPC 를 클릭하여 VPC 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>



#### VPC 생성

VPC 생성은 Project 내 VPC를 생성하는 기능입니다. Project 접근 권한이 필요하며, Project 내 VPC 간 IP 주소 범위는 겹칠 수 없습니다. VPC 는 Project 당 최대 3개 생성 가능합니다.

{% tabs %}
{% tab title="1. 생성 화면 이동" %}
* 왼쪽 메뉴에서 Network > VPC를 선택합니다.
* VPC 목록 화면이 나타나면 상단 메뉴 중 생성 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (54).png" alt=""><figcaption></figcaption></figure>

* VPC 생성을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. VPC 생성" %}
**필수 입력 사항**

* VPC 이름 : 생성될 VPC 의 이름입니다. 3byte\~20byte 이내로 영문 및 숫자, '-' 만 입력 가능합니다.
* IP 주소 범위 : 생성될 VPC 의 IP 주소 범위입니다. (Mask Bit 범위 : 16\~24)

선택 입력 사항

* 설명 : VPC 에 대한 상세한 설명입니다.

<figure><img src="../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

* 팝업 창 우측 하단의 생성 버튼을 클릭합니다.
* 팝업 창이 닫히고, VPC 목록 화면에 생성한 VPC가 목록에 추가된 것이 확인됩니다
{% endtab %}
{% endtabs %}



#### VPC 수정

VPC 정보를 수정하는 기능입니다. VPC 이름과 IP 주소범위(CIDR)는 수정이 불가능합니다.

{% tabs %}
{% tab title="1. 수정 화면 이동" %}
* 왼쪽 메뉴에서 Network > VPC를 선택합니다.
* VPC 목록 화면이 나타나면 수정하려는 VPC를 선택한 후 상단의 수정 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

* VPC 수정을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. VPC 수정" %}
* 설명 항목을 수정합니다.

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

* 수정이 끝나면 팝업 창 하단 오른쪽의 수정 버튼을 클릭합니다.
* 팝업 창이 닫히고, VPC 목록 화면에 수정한 내용이 반영되어 보입니다.
{% endtab %}
{% endtabs %}



#### VPC 삭제

VPC 삭제는 Project 내 VPC 를 삭제하는 기능입니다. 삭제 대상 VPC 하위에 Subnet 이 존재하지 않아야 VPC 를 삭제할 수 있습니다.

{% tabs %}
{% tab title="1. 삭제 화면 이동" %}
* 왼쪽 메뉴에서 Network > VPC를 선택합니다.
* 삭제하려는 VPC를 선택합니다.
* VPC 목록 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (162).png" alt=""><figcaption></figcaption></figure>

* VPC 삭제을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. VPC 삭제" %}
* 팝업 창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (199).png" alt=""><figcaption></figcaption></figure>

* 삭제 팝업 창이 닫히고, VPC 목록에서 삭제되었는지 확인합니다.
{% endtab %}
{% endtabs %}



## FAQ

> **Q. VPC 생성이 되지 않습니다.**
>
> A. [VPC 생성](vpc.md#vpc)을 참고해주시기 바랍니다. 만약 해결 되지 않는다면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.

> **Q. VPC 삭제가 되지 않습니다.**&#x20;
>
> A. [VPC 삭제](vpc.md#vpc-2)를 참고해주시기 바랍니다. 만약 해결 되지 않는다면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.

> **Q. VPC 는 몇 개까지 생생 가능한가요?**
>
> A. VPC 는 Project 당 최대 3개 생성 가능합니다.

