# Gateway Info

## 개요

#### 소개

Gateway Info 는 Gateway 생성에 필요한 정보를 관리합니다. Gateway 생성 시 여기서 생성한 Gateway를 선택되며, 중복 사용이 불가능합니다.

Gateway Info를 생성할 때 Gateway에서 사용할 네트워크 인터페이스를 선택하게 되는데, 지원하는 인터페이스 유형은 다음과 같습니다.&#x20;

#### Interface 유형

<table><thead><tr><th width="168">유형</th><th>설명</th></tr></thead><tbody><tr><td>Routed</td><td>L3 Switch Port 의 Routed Interface 유형으로 자세한 내용은 <a href="https://www.cisco.com/c/en/us/td/docs/switches/datacenter/nexus5000/sw/interfaces/521_N11/b_5k_Interfaces_Config_Guide_Release_521N11/b_5k_Interfaces_Config_Guide_Release_521N11_chapter_011.pdf">여기</a>를 참고해주시기 바랍니다.</td></tr><tr><td>Sub Interface</td><td>L3 Switch Port 의 Sub Interface 유형으로 자세한 내용은 <a href="https://www.cisco.com/c/en/us/td/docs/switches/datacenter/nexus5000/sw/interfaces/521_N11/b_5k_Interfaces_Config_Guide_Release_521N11/b_5k_Interfaces_Config_Guide_Release_521N11_chapter_011.pdf">여기</a>를 참고해주시기 바랍니다.</td></tr><tr><td>SVI</td><td>L3 Switch Port 의 SVI(Switch Virtual Interface) 유형으로 자세한 내용은 <a href="https://www.cisco.com/c/en/us/td/docs/switches/datacenter/nexus5000/sw/interfaces/521_N11/b_5k_Interfaces_Config_Guide_Release_521N11/b_5k_Interfaces_Config_Guide_Release_521N11_chapter_011.pdf">여기</a>를 참고해주시기 바랍니다.</td></tr></tbody></table>

#### Gateway Info 정보 활용 예시 (Gateway 생성 시)

아래 테이블과 같이 구성된 Gateway Info 'GW-Info' 가 있습니다.

<table><thead><tr><th width="227">속성</th><th>값</th></tr></thead><tbody><tr><td>Gateway Info 이름</td><td>GW-Info</td></tr><tr><td>Gateway 유형</td><td>External Gateway</td></tr><tr><td>Interface 유형</td><td>SVI</td></tr><tr><td>PathGroup 이름</td><td>EXT-PG</td></tr><tr><td>vlan 번호</td><td>1000</td></tr><tr><td>PathEndpoint 구성1<br>(PathEndpoint 구성 내역)</td><td><p>유형 : PORT</p><p>PathEndpoint : PathEp1<br>IP Address 1 : 10.20.30.0/24</p></td></tr><tr><td>Node 정보1<br>(Node 정보)</td><td>이름 : Node1<br>Router Id : 1.1.1.1<br>Static Route : 10.0.0.0/8<br>Next Hop Ip : 10.20.30.1/24</td></tr></tbody></table>

GW-Info 의 Gatetway 유형이 External Gateway 이므로 [External Gateway 생성](../network/gateway.md#external-gateway-1) 시 사용 가능합니다.\
GW-Info 를 이용하여 External Gateway 'EXT-GW' 를 생성하면, 'EXT-GW' 와 [External Gateway 연결](../network/routing/gateway-routing.md)을 통해 10.0.0.0/8 대역을 가진 외부 네트워크와 통신이 가능하게 됩니다. 이 때 Border Leaf 는 Node1 이 되고, 외부 네트워크와 접점이 되는 인터페이스는 PathEp1 이 됩니다. 그리고 이를 통해 나가는 Traffic 은 1000번 vlan 으로 Encap 됩니다. **단, 외부 네트워크에서 ACI Network 를 인식할 수 있도록 라우팅 테이블을 설정하는 사전 작업이 필요합니다.**



## 사용 가이드

#### Gateway Info 목록 조회

왼쪽 메뉴에서 Fabric 관리 > Gateway Info 를 클릭하여 Gateway Info 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure>



#### Gateway Info 생성

Gateway 생성 시 필요한 정보를 생성하는 기능입니다. Gateway Info를 생성하기 위해선 Gateway 유형의 [PathGroup](pathgroup.md) 이 사전에 등록되어 있어야 합니다.

{% tabs %}
{% tab title="1. 생성 화면 이동" %}
* 왼쪽 메뉴에서 Fabric 관리 > Gateway Info 을 선택합니다.
* Gateway Info 목록이 나타나면 상단 메뉴 중 생성 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (119).png" alt=""><figcaption></figcaption></figure>

* Gateway Info 생성을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. Gateway Info 생성" %}
1. **(필수)** Gateway Info 이름을 입력합니다.
2. **(필수)** Gateway 유형을 선택합니다. 현재는 External Gateway 만 선택 가능합니다.
3. **(필수)** [Interface 유형](gateway-info.md#interface)을 선택합니다. Interface 유형으로 Routed, SVI, Sub Interface 선택 가능하며, SVI 나 Sub Interface를 선택하는 경우, vlan 번호를 반드시 입력해야합니다.
4. **(필수)** [PathGroup](pathgroup.md) 정보를 선택합니다.
   * PathGroup 이름을 선택하면 [PathEndpoint](pathendpoint.md) 구성 내역이 자동으로 채워집니다.
   * PathEndpoint 별 IP Address 를 입력합니다. \
     유형이 Port 인 경우 1개를 입력하고, VPC 인 경우 2개를 입력합니다.
5. **(필수)** Node 정보를 입력합니다.
   * Node 정보는 추가 버튼을 눌러 테이블 목록 형태로 복수 개 구성이 가능합니다.
   * 목록에 추가하고자 할 경우,  Leaf Node 이름, Router Id, Static Route, Next Hop Ip 정보를 입력한 다음 추가 버튼을 클릭합니다.
   * 등록된 정보를 삭제하고자 할 경우, 🗑 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>

* 팝업 창 우측 하단의 생성 버튼을 클릭합니다.
* 팝업 창이 닫히고, Gateway Info 목록 화면에 생성한 Gateway Info가 추가된 것을 확인합니다.
{% endtab %}
{% endtabs %}



#### Gateway Info 수정

{% tabs %}
{% tab title="1. 수정 화면 이동 및 Gateway Info 수정" %}
* 왼쪽 메뉴에서 Fabric 관리 > Gateway Info 를 선택합니다.
* Gateway Info 목록 화면이 나타나면 수정하려는 Gateway Info을 선택한 다음, 상단의 수정 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>

* Gateway Info 수정 팝업 창이 화면에 나타납니다.

<figure><img src="../.gitbook/assets/GatewayInfo_modify (1).webp" alt=""><figcaption></figcaption></figure>

* [Gateway Info 생성](gateway-info.md#2.-gateway-info) 을 참고하여 원하는 내용을 수정 후, 팝업 창 우측 하단의 수정 버튼을 클릭합니다.
* 팝업 창이 닫히고, 수정 사항이 Gateway Info 목록에 반영되어 조회됩니다.
{% endtab %}
{% endtabs %}



#### Gateway Info 삭제

Gatway Info 삭제는 Gatway Info 를 삭제하는 기능입니다. '사용 중' 상태의 Gateway Info 는 삭제할 수 없습니다.

{% tabs %}
{% tab title="1. 삭제 화면 이동" %}
* 왼쪽 메뉴에서 Fabric 관리 > Gateway Info 을 선택합니다.
* Gateway Info 목록 화면이 나타나면 삭제하려는 Gateway Info를 선택한 다음, 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (110).png" alt=""><figcaption></figcaption></figure>

* Gateway Info 삭제 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. Gateway Info 삭제" %}
* 팝업 창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (124).png" alt=""><figcaption></figcaption></figure>

* 삭제 팝업 창이 닫히고, Gateway Info 목록에서 삭제되었는지 확인합니다.
{% endtab %}
{% endtabs %}



## FAQ

> **Q. Gateway Info 생성이 되지 않습니다.**
>
> A. [Gateway Info 생성](gateway-info.md#gateway-info) 을 참고해주시기 바랍니다. 만약 해결 되지 않는다면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.

> **Q. Gateway Info 삭제가 되지 않습니다.**
>
> A. [Gateway Info 삭제](gateway-info.md#2.-gateway-info-2) 을 참고해주시기 바랍니다. 만약 해결 되지 않는다면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.G
