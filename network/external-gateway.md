# External Gateway 연결

### 개요

#### 소개

External Gateway 와 VPC 내부의 Subnet 간 연결 서비스를 제공합니다.

고객사 네트워크와 통신을 하고자하는 Server 가 위치한 Subent과 고객사 네트워크와 연결한 [External Gateway](external-gateway-1.md)를 연결해야 외부 통신이 가능합니다.&#x20;



### 사용가이드

#### External Gateway 연결 목록 조회

왼쪽 메뉴에서 Network > Routing > External Gateway 연결 을 클릭하여 External Gateway 연결 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>



#### External Gateway 연결 생성

External Gateway 연결은 Subnet 과 External Gateway을 연결하여 양방향 통신을 제공하는 기능입니다. 이를 위해선 하나 이상의 External Gateway 와 Subnet 이 필요합니다. External Gateway 와 연결되는 Subnet IP 주소 범위는 External Gateway 외부 IP 주소 범위 및 해당 External Gateway에 연결된 타 Subnet IP 주소 범위와 중복될 수 없습니다.

{% tabs %}
{% tab title="1. 생성 화면 이동" %}
* 왼쪽 메뉴에서 Network > Routing > External Gateway 연결 을 선택합니다.
* External Gateway 연결 목록이 나타나면, 상단 메뉴 중 생성 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

* External Gateway 연결 생성을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. External Gateway 연결 생성" %}
**필수 입력 사항**

* External Gateway 이름 :  연결 대상 External Gateway를 선택합니다.
* 연결 대상 Subnet 목록 :  External Gateway에 연결할 Subnet으로, 복수 개 선택이 가능합니다.

<figure><img src="../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>

* 팝업 창 우측 하단의 생성 버튼을 클릭합니다.
* 팝업 창이 닫히고, External Gateway 연결 목록 화면에 External Gateway 연결이 새로 추가된 것을 확인합니다.
{% endtab %}
{% endtabs %}



#### External Gateway 연결 삭제&#x20;

{% tabs %}
{% tab title="1. 삭제 화면 이동" %}
* 왼쪽 메뉴에서 Network > Routing > External Gateway 연결 을 선택합니다.
* External Gateway 연결 목록 화면이 나타나면 삭제하려는 External Gateway 연결을 선택한 다음, 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (136).png" alt=""><figcaption></figcaption></figure>

* External Gateway 연결 삭제을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. External Gateway 연결 삭제" %}
* 팝업 창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

* 삭제 팝업 창이 닫히고, External Gateway 연결 목록에서 삭제되었는지 확인합니다.
{% endtab %}
{% endtabs %}

