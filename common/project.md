# Project

## 개요

#### 소개

Project는 서비스 정책 및 리소스를 관리하는 최상위 그룹입니다.\
사용자 계정 당 최대 3개의 Project를 생성할 수 있으며, Project에 구성원을 추가하고 구성원마다 접근 권한을 부여하고 관리할 수 있습니다.

#### Project 유형

다음 3가지 유형의 Project가 존재하며, 일반 사용자가 접근 가능한 Project는 User Project입니다.

<table><thead><tr><th width="173">유형</th><th>설명</th></tr></thead><tbody><tr><td>User</td><td>일반 사용자가 생성한 Project</td></tr><tr><td>Common</td><td>시스템 관리자가 생성한 Project</td></tr><tr><td>NFV</td><td>VNF 서비스를 배포 관리하기 위한 Project</td></tr></tbody></table>

#### Project 구성원 역할 및 권한

Project에는 구성원을 추가, 삭제할 수 있으며, 구성원마다 권한을 설정하여 작업을 제한하게 됩니다.\
Project 구성원 역할에는 owner와 member가 있으며, project 생성자가 owner 역할을 하게 됩니다.\
Project 권한은 관리자 권한인 admin과 사용자 권한인 member가 있으며, project owner는 기본적으로 관리자 권한을 갖게 됩니다. admin 권한을 가진 구성원만 Project 구성원을 추가, 삭제하고 구성원의 권한을 설정할 수 있습니다.&#x20;

<table><thead><tr><th width="179">역할</th><th>설명</th></tr></thead><tbody><tr><td>owner</td><td>Project 생성자</td></tr><tr><td>member</td><td>Project 구성</td></tr></tbody></table>

<table><thead><tr><th width="177.33333333333331">권한</th><th>설명</th></tr></thead><tbody><tr><td>project_admin</td><td><p>Project 관리자 권한</p><p>Project 수정과 삭제가 가능하며, owner는 기본적으로 관리자 권한을 갖습니다. </p></td></tr><tr><td>project_member</td><td>Project 사용자 권한<br>Project 수정과 삭제가 불가합니다. </td></tr></tbody></table>

## 사용 가이드

#### Project 목록 조회

* 왼쪽 상단의 Project 메뉴명 옆의 more 아이콘 ![](<../.gitbook/assets/image (204).png>)을 클릭하여 나오는 목록 관리 메뉴를 클릭합니다.
* 콘텐츠 영역에 사용자가 참여하고 있는 Project의 목록이 조회됩니다.

<div align="center">

<figure><img src="../.gitbook/assets/스크린샷 2023-03-07 오전 8.59.03 (1).png" alt=""><figcaption></figcaption></figure>

</div>

#### Project 전환

여러 Project에 참여하고 있을 경우, 한번에 한 개의 Project에서만 작업이 가능하므로 작업하고자 하는 Project로 전환하는 절차가 필요합니다.

* 왼쪽 상단의 Project 메뉴명 밑의 콤보박스를 클릭합니다.
* 콤보박스 목록에서 작업하고자 하는 Project를 선택합니다.

<figure><img src="../.gitbook/assets/스크린샷 2023-03-07 오전 9.03.23.png" alt=""><figcaption></figcaption></figure>

#### Project 생성

{% tabs %}
{% tab title="1. Project 생성화면 이동" %}
* [Project 목록 조회](project.md#project-3) 가이드에 따라 Project 관리 화면으로 이동합니다.
* Project 목록 상단의 +생성 버튼을 클릭합니다.
* Project 생성을 위한 팝업 창이 나타납니다.

<figure><img src="../.gitbook/assets/image (188).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="2. Project 정보 입력" %}
* Project 이름을 입력합니다. 이름은 3byte 이상 20byte 이내로 작성하며 영문과 숫자, '-'만 사용 가능합니다.
* 필요 시 [Project 구성원을 추가](project.md#3.)합니다.
* 필요 시 Project 설명을 입력합니다. 설명은 최대 100byte 입력 가능합니다.

<figure><img src="../.gitbook/assets/image (197).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="3. 구성원 추가(선택)" %}
Project 구성원 추가는 필수가 아닙니다. 추가하지 않을 경우 생성자만 Project의 구성원이 됩니다.\
Project 구성원을 추가하려면,&#x20;

* Project 구성원 콤보 박스를 클릭합니다.
* 추가하고자 하는 사용자를 선택하고, 오른쪽의 추가 버튼을 클릭합니다.
* 추가한 사용자가 하단의 구성원 목록에 추가되면, 목록의 Project 권한 컬럼에서 사용자에게 부여할 권한을 선택합니다.

<figure><img src="../.gitbook/assets/image (129).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="4. 생성 완료" %}
* Project에 대한 모든 정보를 입력 후 하단의 생성 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>

* 팝업 창이 닫히고, Project 관리 화면에 생성한 Project가 추가되어 조회됩니다.
{% endtab %}
{% endtabs %}



#### Project 수정

Project 수정은 Project의 구성원 추가, 삭제, 권한 변경 및 설명을 변경하는 기능으로, project\_admin 권한을 가진 사용자만 수정할 수 있습니다. Project 이름은 변경이 불가합니다.

{% tabs %}
{% tab title="1. Project 수정화면 이동" %}
* [Project 목록 조회](project.md#project-3) 가이드에 따라 Project 관리 화면으로 이동합니다.
* Project 관리 화면에 조회 된 목록 중 수정하고자 하는 Project를 선택합니다.
* Project 목록 상단의 수정 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (212).png" alt=""><figcaption></figcaption></figure>

* Project 수정을 위한 팝업 창이 나타납니다.
{% endtab %}

{% tab title="2. Project 수정" %}
* [구성원 변경](project.md#2.), 설명 변경을 수행한 후 하단의 수정 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (202).png" alt=""><figcaption></figcaption></figure>

* 팝업 창이 닫히고, Project 목록이 새로 조회 되어 화면에 표시됩니다.
{% endtab %}

{% tab title="3. 구성원 정보 변경" %}
1. 구성원 추가
   * [Project 생성 시 구성원 추가](project.md#3.)와 동일한 절차로 구성원을 추가할 수 있습니다.
2. 구성원 권한 수정
   * Project 구성원  목록에서 수정하려는 구성원의 Project 권한 컬럼을 클릭합니다.
   * 권한 콤보 박스에서 변경하려는 권한을 선택합니다.
3. 구성원 삭제
   * Project 구성원 목록에서 삭제하려는 구성원의 Action 컬럼 휴지통을 클릭합니다.
{% endtab %}
{% endtabs %}



#### Project 삭제

Project 삭제는 project\_admin 권한을 가진 구성원만 수행할 수 있으며, Project 하위에 VPC와 Server가 없는 경우에만 Project를 삭제할 수 있습니다. \
[InitScript](../compute/init-script.md), [KeyPair](../compute/key-pair.md), [SecurityGroup](../compute/security-group.md), [External Gateway](../network/external-gateway-1.md), Internet Gateway를 비롯하여 모든 정보가 Project 삭제 시 함께 삭제되며 복구가 불가능하니 주의가 필요합니다.

{% tabs %}
{% tab title="1. Project 삭제 화면 이동" %}
* [Project 목록 조회](project.md#project-3) 가이드에 따라 Project 관리 화면으로 이동합니다.
* Project 관리 화면에 조회 된 목록 중 삭제하고자 하는 Project를 선택합니다.
* Project 목록의 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (213).png" alt=""><figcaption></figcaption></figure>

* Project 삭제 팝업 창이 화면에 나타납니다.
{% endtab %}

{% tab title="1. Project 삭제" %}
* 삭제하려는 Project 이름을 입력한 다음, 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (133).png" alt=""><figcaption></figcaption></figure>

* 삭제 팝업 창이 닫히고, Project 목록이 새로 조회 되며 Project가 삭제되었는지 확인합니다.
{% endtab %}
{% endtabs %}



## FAQ

> **Q. Project는 몇 개까지 생성이 가능한가요?**
>
> Project는 사용자 계정 당 최대 3개 생성 가능합니다.

> **Q. Project 삭제가 되지 않습니다.**
>
> Project는 관리자(project\_admin) 권한을 가진 사용자만 가능하니 먼저 권한을 확인해야 합니다.
>
> 관리자인데도 삭제가 되지 않으면 Project 하위에 삭제하지 않은 VPC나 Server가 있는지 확인해야 합니다. Project 하위에 VPC나 Server가 있다면 먼저 VPC와 Server를 삭제한 후 Project를 삭제하십시오.
