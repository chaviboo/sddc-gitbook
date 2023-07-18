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

# VNF Package



## 개요

VNF(Virtual Network Functions) 형상을 위한 패키지 파일(\*tar.gz)을 업로드하고, 삭제하는 기능을 제공합니다. 패키지 파일 업로드 시, 상품 유형(현재는 가상 방화벽(vFW)만 제공)과 HA(High Availability) 설정 여부와 VNF Spec을 선택해야 하며 추가적으로 설명을 기입할 수 있습니다. VNF 패키지 파일 수정은 Spec과 설명만 수정 가능합니다. 파일 수정이 필요한 경우, 삭제 후 다른 파일을 업로드 해야 합니다.



## 사용 가이드

#### VNF 패키지 파일 조회



#### VNF 패키지 파일 업로드



#### VNF 패키지 파일 삭제



#### VNF 패키지 파일 수정



## FAQ

> **Q. VNF 패키지 파일 삭제가 되지 않습니다.**
>
> A. VNF 패키지 삭제(링크)를 참고해주시기 바랍니다. 해당 VNF 패키지 파일을 참조하고 있는 NS 패키지 파일(링크)이 있을 경우, 해당 NS 패키지 파일을 먼저 삭제하시고 다시 시도해주시기 바랍니다.
>
>

