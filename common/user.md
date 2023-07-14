# User

## 개요

SDDC 플랫폼에 등록된 User 목록을 관리하는 시스템 관리자용 메뉴입니다.

#### User 정의

SDDC 플랫폼에 접근하는 모든 **계정 단위**을 일컫는 개념입니다.

#### User 권한

User 권한은 **User의 하위 개념**으로<mark style="color:blue;">,</mark> "관리자", "사용자" 두 가지로 구분됩니다.

<table><thead><tr><th width="216">권한</th><th>설명</th></tr></thead><tbody><tr><td>관리자</td><td><p>시스템 관리자 권한입니다.</p><p>공통 관리, Fabric 관리 메뉴에 대한 접근이 가능합니다.</p></td></tr><tr><td>사용자</td><td>일반 사용자 권한입니다.</td></tr></tbody></table>



## 사용 가이드

#### User 목록 조회

왼쪽 메뉴에서 공통 관리 > User 를 클릭하여 User 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>



#### User 등록

{% tabs %}
{% tab title="1. User 등록 화면 이동" %}
* 왼쪽 메뉴에서 공통 관리 > User 를 선택합니다.
* User 목록 화면이 나타나면 상단 메뉴 중 등록 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (102).png" alt=""><figcaption></figcaption></figure>

* User 등록을 위한 팝업 창이 나타납니다.
{% endtab %}

{% tab title="2. User 등록 정보 입력" %}
**필수 입력 사항**

* 아이디 : 사용자 아이디를 입력합니다. 최소 3자리 이상 영문과 숫자만 입력 가능합니다.
* 이름 : 사용자 이름을 입력합니다. 최소 3자리 이상 영문과 국문만 입력 가능합니다.
* 비밀번호 / 비밀번호(확인) : 최소 8자 이상 문자, 숫자, 특수문자($\~!@#$%^&\*\_-+=\`|(){}\[]:;"'<>,.?/)로 구성된 비밀번호를 동일하게 2번 입력합니다.
* 이메일 : 이메일 수신이 가능한 이메일 주소를 입력합니다.
* 전화번호 : 사용자 휴대폰 번호를 입력합니다.

{% hint style="warning" %}
주의

아이디, 이름은 등록 후 수정이 불가능합니다.
{% endhint %}

<figure><img src="../.gitbook/assets/image (205).png" alt=""><figcaption></figcaption></figure>

* 팝업 창 우측 하단의 등록 버튼을 클릭합니다.
* 팝업 창이 닫히고, User 목록 화면에 생성한 User가 추가된 것을 확인합니다.
{% endtab %}
{% endtabs %}

{% hint style="info" %}
참고

User 등록 기능을 통해 추가된 User 권한은 기본적으로 "사용자"입니다.&#x20;

"관리자" 권한이 필요한 경우, 시스템 관리자(sddc.ktcloud@kt.com)에게 별도 요청해야 합니다.
{% endhint %}



#### User 수정

등록된 User 정보를 수정하는 기능입니다. 아이디, 이름은 수정이 불가능 합니다.

{% tabs %}
{% tab title="1. User 수정 화면 이동" %}
* 왼쪽 메뉴에서 공통 관리 > User 를 선택합니다.
* User 목록 화면이 나타나면 수정하려는 User를 선택한 다음, 상단의 수정 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (191).png" alt=""><figcaption></figcaption></figure>

* User 수정을 위한 팝업 창이 나타납니다.
{% endtab %}

{% tab title="2. User 정보 수정" %}
**필수 입력 사항**

* 이메일 : 이메일 수신이 가능한 이메일 주소를 입력합니다.
* 전화번호 : 사용자 휴대폰 번호를 입력합니다.
* 계정 상태 : User의 활성 여부를 설정합니다. 로그인 시 비밀번호 5회 이상 오류가 발생한 경우, 해당 User는 자동 비활성 처리가 됩니다.

<figure><img src="../.gitbook/assets/image (96).png" alt=""><figcaption></figcaption></figure>

* User 정보 변경 후, 팝업창 하단의 수정 버튼을 클릭합니다.
* 수정 팝업 창이 닫히고, User 목록이 새로 조회되며 수정 내역이 잘 반영되었는지 확인합니다.
{% endtab %}
{% endtabs %}



#### User 삭제

{% tabs %}
{% tab title="1. User 삭제 화면 이동" %}
* 왼쪽 메뉴에서 공통 관리 > User 메뉴를 선택합니다.
* User 목록 화면이 나타나면 삭제하려는 User를 선택한 다음, 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>

* User 삭제를 위한 팝업 창이 나타납니다.
{% endtab %}

{% tab title="2. User 삭제" %}
* 팝업 창 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (189).png" alt=""><figcaption></figcaption></figure>

* 삭제 팝업 창이 닫히고, User 목록이 새로 조회되며 User가 삭제되었는지 확인합니다.
{% endtab %}
{% endtabs %}



#### 비밀번호 초기화

관리자의 권한으로 User의 비밀번호를 초기화하는 기능입니다.

{% tabs %}
{% tab title="1. 비밀번호 초기화 화면 이동" %}
* 왼쪽 메뉴에서 공통 관리 > User 를 선택합니다.
* User 목록 화면이 나타나면 비밀번호를 초기화하고자 하는 User를 선택한 다음, 상단의 비밀번호 초기화 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (121).png" alt=""><figcaption></figcaption></figure>

* 비밀번호 초기화 팝업 창이 나타납니다.
{% endtab %}

{% tab title="2. 비밀번호 초기화" %}
* 팝업 창 하단의 비밀번호 초기화 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (163).png" alt=""><figcaption></figcaption></figure>

* 비밀번호 초기화 팝업 창이 닫히고, 선택한 User의 비밀번호는 User 아이디와 동일하게 설정됩니다.
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
주의

비밀번호가 초기화된 User는 반드시 개인정보 수정 기능을 통해 새 비밀번호로 변경해야 합니다.
{% endhint %}



## FAQ

> **Q. 비밀번호를 변경하는 기능이 보이지 않습니다.**
>
> User 메뉴에서 시스템 관리자는 비밀번호 초기화만 가능하고, 비밀번호 변경은 불가능합니다.
>
> 비밀번호 변경은 로그인한 User의 개인정보 수정 기능을 통해 개별적으로 수행할 수 있습니다.
>
> * 로그인 > 상단 오른쪽 사용자 아이콘 클릭 > 계정관리 클릭 > 개인정보 수정 - 비밀번호 변경 버튼 클릭

