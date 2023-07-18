---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Service Graph

## 개요

#### 소개

Service Graph 는 vWAF, vFW 등 NFV 서비스를 의미합니다. 등록된 Service Graph는 Routing에 [PBR 연결](../../network/subnet-routing.md#pbr)하여 사용할 수 있습니다. 현재 SDDC Platform 에서 Service Graph를 생성할 수는 없고 사전에 등록된 정보하거나 삭제만 할 수 있습니다.

#### 구성

<table><thead><tr><th width="190">속성</th><th width="337">설명</th><th width="94">필수 여부</th><th>수정 가능 여부</th></tr></thead><tbody><tr><td>Service Graph 이름</td><td>Service Graph 의 이름입니다.</td><td>O</td><td>X</td></tr><tr><td>식별자</td><td>Service Graph 의 ACI Object 식별자입니다.</td><td>O</td><td>X</td></tr><tr><td>Filter</td><td>Service Graph 에 적용된 Filter 정보입니다. Filter 에 허용된 Traffic 만 Service Graph가 적용됩니다.</td><td>O</td><td>X</td></tr><tr><td>상태</td><td>Service Graph의 등록 상태 정보입니다. Registered 상태의 Service Graph 만 사용 가능합니다.</td><td>O</td><td>X</td></tr><tr><td>설명</td><td>Service Graph의 상세한 설명입니다.</td><td>X</td><td>X</td></tr></tbody></table>



## 사용 가이드

#### Service Graph 삭제

{% tabs %}
{% tab title="1. 삭제 화면 이동" %}
* 왼쪽 메뉴에서 Fabric 관리 > Service Graph 을 선택합니다.
* Service Graph 목록 화면이 나타나면 삭제하려는 Service Graph을 선택한 다음, 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (156).png" alt=""><figcaption></figcaption></figure>

* Service Graph 삭제 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. Service Graph 삭제" %}
* 팝업 창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (193).png" alt=""><figcaption></figcaption></figure>

* 삭제 팝업 창이 닫히고, Service Graph 목록에서 삭제되었는지 확인합니다.


{% endtab %}
{% endtabs %}

{% hint style="info" %}
참고

SDDC Platform 에서 Service Graph 를 삭제하더라도 ACI 에 등록된 정보가 삭제되지 않습니다.
{% endhint %}



## FAQ

> **Q. Service Graph 에 조회되는 목록이 없습니다.**
>
> A. ACI 에 Service Graph 등록 작업이 필요합니다. 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.
