# Key Pair

## 개요

**소개**

Key Pair는 SSH Private, Public Key Pair를 생성하여 Server 연결할 때 자격 증명 입증에 사용하는 서비스입니다. Public Key는 사용될 Server에 설정하고, Private Key는 사용자가 접속 가능하도록 구성할 수 있습니다. 생성된 Private Key는 1회만 다운로드 가능하므로 주의하여 관리하시기 바랍니다.&#x20;



## 사용 가이드

**Key Pair 목록 조회**

왼쪽 메뉴에서 Compute > Key Pair 를 클릭하여 Key Pair목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (91).png" alt=""><figcaption></figcaption></figure>



**Key Pair 생성**

{% tabs %}
{% tab title="1. 생성 탭 이동" %}
* Compute -> Key Pair 메뉴로 이동합니다.
* Key Pair 목록의 상단의 생성 버튼을 클릭합니다.

{% hint style="warning" %}
주의

* Key Pair 이름은 3byte 이상 20byte 이내, 영문과 숫자, '-'만 사용 가능합니다.
* 동일 프로젝트에서 동일 이름의 Key Pair는 생성할 수 없습니다.
{% endhint %}

<figure><img src="../.gitbook/assets/image (94).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="2. Key Pair 생성" %}
* Key Pair의 이름을 작성합니다.
* 팝업 창 우측 하단의 생성 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="3. Private Key 다운로드" %}
* Key Pair 생성 완료 시 Private Key가 자동으로 다운로드됩니다.

{% hint style="warning" %}
주의

* 생성된 Priavte Key는 분실 시 복구가 불가능합니다.
* 다운 받은 Private Key는 반드시 안전한 곳에 저장하시기 바랍니다.
{% endhint %}

<figure><img src="../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}



**Key Pair 삭제**

{% tabs %}
{% tab title="1. 삭제 탭 이동" %}
* Compute -> Key Pair 메뉴로 이동합니다.
* 삭제할 Key Pair를 선택합니다.
* Key Pair 목록 상단의 삭제 버튼을 클릭합니다.

{% hint style="warning" %}
주의

Key Pair 삭제 시, 복구가 불가능합니다.
{% endhint %}

<figure><img src="../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="2. Key Pair 삭제" %}
* 팝업 창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (73).png" alt=""><figcaption></figcaption></figure>

* 삭제 팝업 창이 닫히고, Key Pair 목록에서 삭제되었는지 확인합니다.
{% endtab %}
{% endtabs %}



## FAQ

> **Q. Key Pair 비밀번호를 잃어버리면 어떻게 하나요?**
>
> Key Pair 비밀번호 복구는 불가능합니다. 따라서 해당 Key Pair를 삭제 후 다시 생성해야만 합니다.\
> 이미  적용된 Server의 경우 시스템 관리자를 통해 새롭게 생성된 Key Pair로 변경해야 합니다.

> **Q. Key Pair를 삭제할 경우 기존 Server는 어떻게 되나요?**
>
> 콘솔에서  Key Pair를 삭제하더라도 기존에 적용된  Server에서는 사용이 가능합니다.

> **Q. Server의 Key Pair를 변경할 수 있나요?**
>
> Server 생성 시 적용한 Key Pair는 수정이 불가능합니다.
>
> 변경을 원하시면 시스템 관리자에게 문의바랍니다.
