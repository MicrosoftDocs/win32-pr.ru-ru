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
# <a name="winrm-constants-and-enumerations"></a><span data-ttu-id="cce47-103">Константы и перечисления WinRM</span><span class="sxs-lookup"><span data-stu-id="cce47-103">WinRM Constants and Enumerations</span></span>

<span data-ttu-id="cce47-104">Служба удаленного управления Windows имеет битовые флаги, используемые при создании сеансов и перечислений, а для типов доступа и проверки подлинности на прокси-сервере.</span><span class="sxs-lookup"><span data-stu-id="cce47-104">Windows Remote Management has bit flags used in creating sessions and enumerations, and for access types and authentication to a proxy server.</span></span> <span data-ttu-id="cce47-105">В следующем списке перечислены различные битовые флаги.</span><span class="sxs-lookup"><span data-stu-id="cce47-105">The following list lists the different bit flags.</span></span>

<dl> <dt>

<span data-ttu-id="cce47-106"><span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[Константы сеанса](session-constants.md)</span><span class="sxs-lookup"><span data-stu-id="cce47-106"><span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[Session Constants](session-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="cce47-107">Флаги, используемые в параметре *flags* методов [**WSMan. CreateSession**](wsman-createsession.md) или [**ивсман:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) .</span><span class="sxs-lookup"><span data-stu-id="cce47-107">Flags used in *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) or [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) methods.</span></span>

</dd> <dt>

<span data-ttu-id="cce47-108"><span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**Константы перечисления**](enumeration-constants.md)</span><span class="sxs-lookup"><span data-stu-id="cce47-108"><span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**Enumeration Constants**](enumeration-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="cce47-109">Флаги, используемые в параметре *flags* для Call в [**Session. Enumerate**](session-enumerate.md) или [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="cce47-109">Flags used in *flags* parameter of call to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

</dd> <dt>

<span data-ttu-id="cce47-110"><span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**всманпроксяусентикатионфлагс**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)</span><span class="sxs-lookup"><span data-stu-id="cce47-110"><span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**WSManProxyAuthenticationFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)</span></span>
</dt> <dd>

<span data-ttu-id="cce47-111">Флаги, используемые в параметре *authenticationMechanism* вызова [**IWSManConnectionOptionsEx2:: сетпрокси**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).</span><span class="sxs-lookup"><span data-stu-id="cce47-111">Flags used in *authenticationMechanism* parameter of call to [**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).</span></span>

</dd> <dt>

<span data-ttu-id="cce47-112"><span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**всманпроксякцесстипефлагс**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)</span><span class="sxs-lookup"><span data-stu-id="cce47-112"><span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**WSManProxyAccessTypeFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)</span></span>
</dt> <dd>

<span data-ttu-id="cce47-113">Флаги, используемые в параметре *акцесстипе* вызова [**IWSManConnectionOptionsEx2:: сетпрокси**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).</span><span class="sxs-lookup"><span data-stu-id="cce47-113">Flags used in *accessType* parameter of call to [**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="cce47-114">См. также</span><span class="sxs-lookup"><span data-stu-id="cce47-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cce47-115">Справочник по служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="cce47-115">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dt>

[<span data-ttu-id="cce47-116">**WSMan. CreateSession**</span><span class="sxs-lookup"><span data-stu-id="cce47-116">**WSMan.CreateSession**</span></span>](wsman-createsession.md)
</dt> <dt>

[<span data-ttu-id="cce47-117">**Ивсман:: CreateSession**</span><span class="sxs-lookup"><span data-stu-id="cce47-117">**IWSMan::CreateSession**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)
</dt> <dt>

[<span data-ttu-id="cce47-118">**IWSManConnectionOptionsEx2:: Сетпрокси**</span><span class="sxs-lookup"><span data-stu-id="cce47-118">**IWSManConnectionOptionsEx2::SetProxy**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)
</dt> </dl>

 

 




