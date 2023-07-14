# External Gateway

## 개요

**소개**

External Gateway는 고객 네트워크와 SDDC Platform의 네트워크를 손쉽게 연결하는 서비스로, 클라우드 환경 내 여러 VPC와 고객 네트워크간의 연결 허브 역할을 수행하는 게이트웨이 서비스입니다. External Gateway 서비스를 통하여 고객이 원하는 다양한 네트워크 토폴로지 구성이 가능하며,  각각의 VPC 와 External Gateway간 연결된 네트워크 구간은 독립적인 트래픽이 흐르도록 구성됩니다.



## 사용가이드

#### External Gateway 목록 조회

왼쪽 메뉴에서 Network > External Gateway 를 클릭하여 External Gateway 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>



#### External Gateway 생성

{% tabs %}
{% tab title="1. 생성 화면 이동 " %}
* 왼쪽 메뉴에서 Network > External Gateway 을 선택합니다.
* External Gateway 목록이 나타나면 상단 메뉴 중 생성 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

* External Gateway 생성을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. External Gateway 생성" %}
**필수 입력 사항**

* Gateway 이름 : Gateway 의 이름을 입력합니다.
* Gateway Info : 연결 대상인 외부 접점을 선택합니다.
  * Gateway Info는 프로젝트 관리자가 관리자 메뉴 [Gateway Info](../fabric/gateway-info.md)에서 생성해놓은 정보를 활용합니다.&#x20;

<figure><img src="../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

* 팝업 창 우측 하단의 생성 버튼을 클릭합니다.
* 팝업 창이 닫히고, External Gateway 목록 화면에 생성한 External Gateway가 추가된 것을 확인합니다.
{% endtab %}
{% endtabs %}



#### External Gateway 삭제

{% tabs %}
{% tab title="1. 삭제 화면 이동" %}
* 왼쪽 메뉴에서 Network > External Gateway 을 선택합니다.
* External Gateway 목록이 나타나면 상단 메뉴 중 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (222).png" alt=""><figcaption></figcaption></figure>

* External Gateway 삭제를 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. External Gateway 삭제" %}
* 팝업 창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (199).png" alt=""><figcaption></figcaption></figure>

* 삭제 팝업 창이 닫히고, External Gateway 목록에서 삭제되었는지 확인합니다.

{% hint style="warning" %}
주의

Subnet과 연결중인 External Gateway를 삭제할 경우, 외부 통신이 중단됩니다.
{% endhint %}
{% endtab %}
{% endtabs %}

