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

# Volume Snapshot

## 개요

#### 소개

스냅샷을 생성하여 스토리지 데이터를 저장할 수 있습니다. 생성된 스냅샷을 사용하여 원하는 서버에 새로운 스토리지를 생성하면 저장된 데이터가 복구됩니다.



## 사용가이드

#### Block Snapshot 목록조회

왼쪽 메뉴에서 Storage > Block Storage > Block Snapshot 을 클릭하여 Block Snapshot 목록을 조회합니다.



<mark style="color:blue;">**\[이미지 첨부]**</mark>

#### Block Snapshot 생성

{% tabs %}
{% tab title="First Tab" %}
* 왼쪽 메뉴에서 Storage > Block Storage > Volume 을 선택합니다.
* Volume 목록이 나타나면 상단 메뉴 중 스냅샷 생성 버튼을 클릭합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>

* Block Snapshot 생성을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="Second Tab" %}
**필수 입력 항목**

* &#x20;Block Snapshot 이름 : 이름은 영문과 숫자로 3Byte 이상 20Byte 이내로 작성해야하며 특수문자는 "-" 만 가능합니다

<mark style="color:blue;">**\[이미지 첨부]**</mark>
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
주의

Volume이 서버에 연결된 상태에서 Block Snapshot을 생성하면 스냅샷의 데이터가 손상될 수 있습니다.
{% endhint %}

#### Block Snapshot 수정

{% tabs %}
{% tab title="First Tab" %}
* 왼쪽 메뉴에서 Storage > Block Storage > Block Snapshot 을 선택합니다.
* Block Snapshot 목록 화면이 나타나면 수정하려는 Block Snapshot을 선택한 다음, 상단의 수정 버튼을 클릭합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>

* Block Snapshot 수정을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="Second Tab" %}
* Block Snapshot 이름을 수정합니다.
* Block Snapshot 이름 수정 후, 팝업 창 우측 하단의 수정 버튼을 클릭 합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>

* 팝업 창이 닫히고, 수정 사항이 목록에 반영되어 조회됩니다.
{% endtab %}
{% endtabs %}

#### Block Snapshot 삭제

{% tabs %}
{% tab title="First Tab" %}
* 왼쪽 메뉴에서 Storage > Block Storage > Block Snapshot 을 선택합니다.
* Block Snapshot 목록 화면이 나타나면 삭제하려는 Block Snapshot을 선택한 다음, 상단의 삭제 버튼을 클릭합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>

* Block Snapshot 삭제을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="Second Tab" %}
* 팝업 창 우측 하단의 삭제 버튼을 클릭합니다.

<mark style="color:blue;">**\[이미지 첨부]**</mark>

* 삭제 팝업 창이 닫히고, Block Snapshot 목록에서 삭제되었는지 확인합니다.
{% endtab %}
{% endtabs %}

## FAQ

> **Q. Snapshot 상태가 ERROR\_DELETING 인 경우, 삭제가 불가능 하나요??**
>
> 네. 삭제가 불가능하며 관리자에게 문의 부탁드립니다.
