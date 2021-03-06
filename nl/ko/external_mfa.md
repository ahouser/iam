---

copyright:

  years: 2018, 2019

lastupdated: "2019-01-30"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}

# 사용자에 대한 외부 인증 MFA 주문
{: #external}

올바른 액세스를 가진 관리자는 사용자 로그인을 위해 외부 인증을 주문하고 다단계 인증(MFA) 옵션을 사용으로 설정할 수 있습니다. 외부 인증 옵션에 대한 월간 요금이 청구됩니다. 이 유형의 다단계 인증(MFA)은 ID 기반 MFA와 달리 설정이 사용되는 계정에만 필요합니다. 자세한 정보는 [다단계 인증 유형](/docs/iam?topic=iam-types#types)을 참조하십시오.
{:shortdesc}

## 외부 인증 주문
{: #ordering}

다음 액세스 권한이 있는 경우 사용자에 대한 외부 인증을 주문할 수 있습니다.

* 사용자 관리 서비스에 대한 편집자 이상의 역할
* 사용자에 대한 클래식 인프라 계층에서 조상이며 사용자 클래식 인프라 관리 권한이 지정됨

외부 인증을 주문하려면 다음 단계를 완료하십시오.

1. 메뉴 표시줄에서 **관리** &gt; **액세스(IAM)**를 클릭하고 **사용자**를 선택하십시오.
2. 목록에서 사용자를 선택하십시오.
3. **사용자 세부사항** 페이지의 사용자 로그인 관리 섹션에서 **외부 인증 주문**을 선택하십시오. 
4. **Symantec Identity Protection** 또는 **전화 기반 ID 보호**를 선택하십시오.
    * Symantec 인증의 경우 사용자는 [Symantec VIP](https://vip.symantec.com/){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg) 앱을 다운로드하고 인증 정보 ID를 확보하여 주문 프로세스를 계속해야 합니다.
    * 전화 기반 인증의 경우 주문을 진행할 수 있지만, 옵션을 사용하려면 먼저 사용자가 [해당 구성을 설정](/docs/account?topic=account-third-party-MFA#third-party-MFA)해야 합니다.
5. 선택을 기준으로, 주문 전에 프롬프트에 따라 가격과 이용 약관을 검토하십시오.
6. **주문**을 클릭하여 선택을 완료하십시오.

Symantec 인증을 주문한 후에 사용자 세부사항 페이지에서 사용자에 대한 옵션을 설정할 수 있습니다. 또한 전화 기반 인증을 주문한 후에 사용자가 이를 구성하면 사용자 세부사항 페이지에서 사용자에 대한 옵션을 설정할 수 있습니다.

## 외부 인증 옵션 사용 안함으로 설정
{: #disable}

언제든 사용자에 대해 Symantec 또는 전화 기반 MFA를 사용 안함으로 설정할 수 있습니다.

1. 메뉴 표시줄에서 **관리** &gt; **액세스(IAM)**를 클릭하고 **사용자**를 선택하십시오.
2. 목록에서 사용자를 선택하십시오.
3. **사용자 세부사항** 페이지에서 **Symantec 인증** 또는 **전화 기반 인증** 옵션을 설정 해제하십시오. 

## 외부 인증 옵션 취소
{: #cancel}

올바른 액세스를 가진 경우 언제든 외부 인증 주문을 취소할 수 있습니다. 환불 없이 즉시 취소하도록 선택하거나 주문한 시점으로부터 1년 후에 취소하도록 선택할 수 있습니다.

외부 인증 주문을 취소하려면 계정 소유자이거나 다음 액세스를 모두 갖고 있어야 합니다.

* 사용자 클래식 인프라 관리 권한
* 서비스 클래식 인프라 취소 권한
* 지원 센터 계정 관리 서비스를 위한 관리자 또는 [마이그레이션된 권한 액세스 그룹](/docs/iam?topic=iam-predefined#predefined) 내에서 사용할 수 없는 티켓 마이그레이션 클래식 인프라 보기, 편집 및 추가 권한.

외부 인증 주문을 취소하려면 다음 단계를 완료하십시오.

1. 메뉴 표시줄에서 **관리** &gt; **액세스(IAM)**를 클릭하고 사용자를 선택하십시오.
2. 목록에서 사용자를 선택하십시오.
3. **사용자 세부사항** 페이지에서, 주문한 항목에 따라 **Symantec 인증** 또는 **전화 기반 인증** 행에 대해 **삭제** ![삭제 아이콘](../icons/icon_trash.svg)를 클릭하십시오. 
4. 제거하는 경우 선택하십시오.
5. **제거**를 클릭하십시오.
