# Server

## 개요

Server 를 생성, 삭제, 동작제어 등을 제공하는 기능입니다.&#x20;

{% hint style="info" %}
참고\
Server 를 생성하기 위해서는 관련된 VPC, Subnet, Keypair 등이 선행적으로 생성되어 있어야 합니다.
{% endhint %}



## 사용 가이드

#### Server 목록 조회

왼쪽 메뉴에서 Compute > Server 를 클릭하여 Server 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (153).png" alt=""><figcaption></figcaption></figure>



#### **Server 상세보기**

Server 목록화면에서 특정 Server를 선택하면 상세정보를 확인할 수 있습니다.

<figure><img src="../.gitbook/assets/image (85).png" alt=""><figcaption></figcaption></figure>



#### Server 생성

{% tabs %}
{% tab title="1. 기본사항 입력" %}
Server 생성에 필요한 기본 정보를 설정합니다.

* **Server 이름**: 3byte 이상 20byte 이내, 영문과 숫자, '-' 만 가능합니다.
* **Server Type**: [Flavor](broken-reference)에서 정의한 CPU/RAM 등 서버 구성 유형을 선택합니다.



Server 생성 시 사용할 OS 이미지를 선택합니다.

* **OS 이미지 선택**: [Image](broken-reference)에 등록된 목록이 조회되며, 이 중 원하는 이미지를 선택합니다.



<figure><img src="../.gitbook/assets/image (211).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="2. 네트워크 설정" %}
Server의 네트워크를 설정합니다.

* VPC&#x20;
  * 생성된 VPC가 없을 경우 [VPC](../network/vpc.md)를 참조해 먼저 생성을 진행합니다.
* Subent
  * 생성된 Subnet이 없을 경우 [Subnet](../network/subnet.md)를 참조해 먼저 생성을 진행합니다.
* (Security Group)&#x20;
  * Subnet 선택 시 자동선택됩니다.
* DHCP 여부
  * DHCP 미사용을 선택할 경우 DHCP 주소를 입력하고 IP 검증을 진행합니다.



<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="3. 추가정보 설정" %}
Server 에 관련된 추가정보를 설정합니다.

* 반납보호 여부
  * 반납보호란 Server 삭제 요청 시, 삭제 전에 사용자에게 한번 더 확인하는 과정입니다.
* Key Pair
  * 설정한 Key Pair 를 통해 생성한 Server로 접근할 수 있습니다.
  * 생성된 Key Pair 가 없을 경우 [Key Pair](key-pair.md)를 참조해 생성할 수 있습니다.
* Init Script
  * 직접 입력하거나, 이미 생성되어 있는 Init Script를 불러올 수 있습니다.
  * [Init Script](init-script.md)를 참조해 별도로 생성 및 사용할 수 있습니다.



<figure><img src="../.gitbook/assets/image (203).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="4. 검토 및 생성" %}
Server 생성 요청 전 검토를 진행합니다.

* 설정한 정보가 올바른지 Server 생성 전에 검토를 진행합니다.

검토 결과 이상이 없으면 **SERVER 생성**버튼을 클릭합니다.



<figure><img src="../.gitbook/assets/image (150).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="5. 생성결과 확인" %}
Server 생성결과를 확인합니다.

Server 목록에 생성한 Server가 조회되어 나타납니다.\
생성한 Server의 상태를 통해서 Server 생성 진행상태를 확인할 수 있습니다.



<table><thead><tr><th>Server 상태</th><th width="452">진행상태</th></tr></thead><tbody><tr><td><strong>BUILD</strong></td><td>Server 생성이 진행중입니다.</td></tr><tr><td><strong>ACTIVE</strong></td><td>Server 생성이 완료되었습니다.</td></tr><tr><td><strong>ERROR</strong></td><td>Server 생성을 실패하였습니다.</td></tr></tbody></table>



<figure><img src="../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}



#### Server 동작제어

대상 Server를 선택 한 후 목록 화면 상단에 있는 **희망하는 동작 버튼**을 클릭합니다.

* 제공되는 동작 : 시작, 일시정지, 정지, 재시작, 강제 재시작
* 특정 동작은 특정 Server 상태에서만 수행이 가능합니다.

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>



#### Server 삭제

{% tabs %}
{% tab title="1. Server 삭제 화면 이동" %}
* 왼쪽 메뉴에서 Compute > Server 를 선택합니다.
* Server 목록 화면이 나타나면 삭제하고자 하는 Server를 선택한 다음 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (198).png" alt=""><figcaption></figcaption></figure>

* Server 삭제를 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. Server 삭제" %}
* 삭제하려는 Server 이름을 입력한 다음, 팝업 창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (130).png" alt=""><figcaption></figcaption></figure>

* 팝업 창이 닫히고, Server 목록에서 해당 Server가 삭제된 것을 확인합니다.
{% endtab %}
{% endtabs %}

{% hint style="info" %}
참고

삭제를 희망하는 Server가 반납보호 설정되어 있는 경우, 반납보호 처리를 먼저 진행 후 삭제를 진행할 수 있습니다.
{% endhint %}



#### Server Terminal

대상 Server를 선택 한 후 목록 화면 상단에 있는 **터미널** 버튼을 클릭합니다.

{% tabs %}
{% tab title="1. Server Termial 실행 화면 이동" %}
* 왼쪽 메뉴에서 Compute > Server 를 선택합니다.
* Server 목록 화면이 나타나면, 원하는 Server를 선택한 다음 상단의 터미널 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="2. Server Terminal 시작" %}
* 팝업 창 우측 하단의 시작 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

* 터미널 창이 실행됩니다.
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
주의

Server Terminal 생성 직후 10분간은 다른 사용자가 동일 Server에 대해서 Terminal 대해 접근할 수 없습니다.
{% endhint %}



#### Server 로그

{% tabs %}
{% tab title="1. Server 로그 조회 화면 이동" %}
* 왼쪽 메뉴에서 Compute > Server 를 선택합니다.
* Server 목록 화면이 나타나면, 원하는 Server를 선택한 다음 상단의 로그 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (96).png" alt=""><figcaption></figcaption></figure>

* 로그 조회를 위합 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. Server 로그 조회" %}
* 로그 라인 수를 변경하여 로그 내역을 조회할 수 있습니다. (최대 999,999 라인)

<figure><img src="../.gitbook/assets/image (109).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}



## FAQ

> **Q. 서버 생성 시 ERROR 가 발생합니다.**
>
> A. 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.

> **Q. Server 생성 시 직접 CPU 나 Memory 설정이 가능한가요?**
>
> A. 제공되는 타입만 사용이 가능합니다.

> **Q. Server 생성 시 제공되는 이미지 외에 사용이 가능한가요?**
>
> A. 제공되는 이미지만 사용이 가능합니다.

\
