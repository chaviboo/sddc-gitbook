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

# Init Script

## 개요

서버 생성 시 자동으로 실행할 스크립트를 사용자가 작성할 수 있도록 지원하는 기능입다. 다수의 서버를 생성하면서 동일한 설정이 필요한 경우 Init Script를 만들어서 재활용할 수 있습니다.



## 사용 가이드

#### Init Script 목록 조회

왼쪽 메뉴에서 Compute > Init Script 를 클릭하여 Init Script 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (159).png" alt=""><figcaption></figcaption></figure>



#### Init Script 생성

{% tabs %}
{% tab title="1. Init Script 생성 화면 이동" %}
* 왼쪽 메뉴에서 Compute > Init Script를 선택합니다.
* Init Script 목록 화면이 나타나면 상단 메뉴 중 생성 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

* Init Script 생성을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. Init Script 작성" %}
* Init Script 이름을 입력합니다. 이름은 3byte 이상 20byte 이내의 영문, 숫자, '-' 만 가능합니다.
* Init Script를 작성합니다.&#x20;

{% hint style="warning" %}
주의

* 현재 Linux만 지원합니다.
* Script 맨 첫 줄에   #/bin/bash, #/usr/bin/env python 과 같은 형태로 실행하려는 스크립트 경로를 반드시 입력하시기 바랍니다.
* 한글 및 주석은 입력이 불가합니다.
* Script 자체의 오류 검증은 제공하지 않습니다.
{% endhint %}

* 필요 시 Init Script 설명을 입력합니다.
* 오른쪽 하단의 생성 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (204).png" alt=""><figcaption></figcaption></figure>

* 팝업 창이 닫히고, Init Script 목록 화면에 생성한 Init Script가 목록에 추가되며, 목록에서 확인됩니다
{% endtab %}
{% endtabs %}

{% hint style="info" %}
**Init Script 샘플 - Linux 비밀번호 초기화**

\#!/bin/bash\
echo '1234' | passwd --stdin root
{% endhint %}



#### Init Script 수정

Init Script의 이름, script, 설명을 수정할 수 있습니다. Init Script의 수정 사항은 이미 생성된 Server에는 영향을 주지 않습니다. 만약, 이미 생성한 Server에서 사용하는 Init Script를 수정하려면 Server에 직접 접속하여 수정해야 합니다.

{% tabs %}
{% tab title="1. Init Script 수정 화면 이동" %}
* 왼쪽 메뉴에서 Compute > Init Script를 선택합니다.
* Init Script 목록 화면이 나타나면 수정하려는 Init Script를 선택한 후 상단의 수정 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (175).png" alt=""><figcaption></figcaption></figure>

* Init Script 수정을 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. Init Script 수정" %}
* 이름, script, 설명 중 수정을 원하는 항목을 수정합니다.
* 수정은 생성과 방법이 동일하므로 자세한 사항은 [Init Script 생성](init-script.md#init-script) 을 참고합니다.
* 수정이 끝나면 하단의 수정 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (112).png" alt=""><figcaption></figcaption></figure>

* 팝업 창이 닫히고, Init Script 목록 화면에 수정한 내용이 반영되어 보입니다.
{% endtab %}
{% endtabs %}



#### Init Script 삭제

Init Script 삭제는 이미 생성된 Server의 Init Script를 삭제하지는 않으며, 새로운 Server 생성 시 삭제한 Init Script를  참조할 수 없게 됩니다.

{% tabs %}
{% tab title="1. Init Script 삭제 화면 이동" %}
* 왼쪽 메뉴에서 Compute > Init Script를 선택합니다.
* Init Script 목록 화면이 나타나면 삭제하려는 Init Script를 선택한 후 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (128).png" alt=""><figcaption></figcaption></figure>

* Init Script 삭제를 위한 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="2. Init Script 삭제" %}
* 팝업 창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (77).png" alt=""><figcaption></figcaption></figure>

* 삭제 팝업 창이 닫히고, Init Script 목록 화면에 삭제한 Init Script가 제외되어 보입니다.
{% endtab %}
{% endtabs %}



## FAQ

> **Q. Server 생성 후 Init Script의 실행 결과는 어떻게 확인할 수 있나요?**
>
> Init Script 실행 결과는 Compute > Server 메뉴에서 생성한 Server를 선택한 후 터미널에 접속하거나 최근 로그를 확인 기능을 통해 확인할 수 있습니다.

> **Q. Init Script의 정상적으로 동작하지 않은 것 같습니다. 어떻게 해야 하나요?**
>
> Init Script 자체에 오류가 있는지 먼저 확인하시기 바랍니다. 만약 오류 수정이 필요한 경우 Server에 직접 접속하여 Init Script를 수정해야 합니다.
>
> Init Script의 오류가 없는데도 정상 동작하지 않은 경우는 시스템 관리자(sddc.ktcloud@kt.com)으로 문의하시기 바랍니다.



```
// Some code
```
