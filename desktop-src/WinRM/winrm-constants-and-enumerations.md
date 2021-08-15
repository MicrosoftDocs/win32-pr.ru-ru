---
title: Константы и перечисления WinRM
description: Windows Удаленное управление имеет битовые флаги, используемые при создании сеансов и перечислений, а для типов доступа и проверки подлинности на прокси-сервере.
ms.assetid: 17e59245-26a3-4383-a741-4a09f3cfcec6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73de8f418d5b0fb0bd7adebb8439ccbce67f0bcb6aacf72ed2665683c00e0076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742940"
---
# <a name="winrm-constants-and-enumerations"></a>Константы и перечисления WinRM

Windows Удаленное управление имеет битовые флаги, используемые при создании сеансов и перечислений, а для типов доступа и проверки подлинности на прокси-сервере. В следующем списке перечислены различные битовые флаги.

<dl> <dt>

<span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[Константы сеанса](session-constants.md)
</dt> <dd>

Флаги, используемые в параметре *flags* методов [**WSMan. CreateSession**](wsman-createsession.md) или [**ивсман:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) .

</dd> <dt>

<span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**Константы перечисления**](enumeration-constants.md)
</dt> <dd>

Флаги, используемые в параметре *flags* для Call в [**Session. Enumerate**](session-enumerate.md) или [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

</dd> <dt>

<span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**всманпроксяусентикатионфлагс**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)
</dt> <dd>

Флаги, используемые в параметре *authenticationMechanism* вызова [**IWSManConnectionOptionsEx2:: сетпрокси**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).

</dd> <dt>

<span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**всманпроксякцесстипефлагс**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)
</dt> <dd>

Флаги, используемые в параметре *акцесстипе* вызова [**IWSManConnectionOptionsEx2:: сетпрокси**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).

</dd> </dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Windows Справочник по удаленному управлению](windows-remote-management-reference.md)
</dt> <dt>

[**WSMan. CreateSession**](wsman-createsession.md)
</dt> <dt>

[**Ивсман:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)
</dt> <dt>

[**IWSManConnectionOptionsEx2:: Сетпрокси**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)
</dt> </dl>

 

 




