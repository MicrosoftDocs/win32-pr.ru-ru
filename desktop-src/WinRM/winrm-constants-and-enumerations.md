---
title: Константы и перечисления WinRM
description: Служба удаленного управления Windows имеет битовые флаги, используемые при создании сеансов и перечислений, а для типов доступа и проверки подлинности на прокси-сервере.
ms.assetid: 17e59245-26a3-4383-a741-4a09f3cfcec6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0789d440ff0f88cc037e0dc9e544ca559c1af5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068277"
---
# <a name="winrm-constants-and-enumerations"></a>Константы и перечисления WinRM

Служба удаленного управления Windows имеет битовые флаги, используемые при создании сеансов и перечислений, а для типов доступа и проверки подлинности на прокси-сервере. В следующем списке перечислены различные битовые флаги.

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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по служба удаленного управления Windows](windows-remote-management-reference.md)
</dt> <dt>

[**WSMan. CreateSession**](wsman-createsession.md)
</dt> <dt>

[**Ивсман:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)
</dt> <dt>

[**IWSManConnectionOptionsEx2:: Сетпрокси**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)
</dt> </dl>

 

 




