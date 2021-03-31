---
title: Реализация поддержки NAP In-Band для методов EAP
description: Можно включить для методов протокола EAP для EAPHost, поддерживающих передачу объектов типа length-value (ТЛВС).
ms.assetid: 298c89d9-7a6a-4280-9af9-77c7c00cab92
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9eae9fc17e99b27f620fbab1ed42cbd4b73800
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797112"
---
# <a name="implementing-in-band-nap-support-for-eap-methods"></a><span data-ttu-id="729cc-103">Реализация поддержки NAP In-Band для методов EAP</span><span class="sxs-lookup"><span data-stu-id="729cc-103">Implementing In-Band NAP Support for EAP Methods</span></span>

<span data-ttu-id="729cc-104">Поддержку [защиты доступа к сети](/windows/desktop/NAP/network-access-protection-start-page) (NAP) для метода EAP можно включить для методов протокола EAP, поддерживающих передачу объектов типа length-value (ТЛВС).</span><span class="sxs-lookup"><span data-stu-id="729cc-104">In-band [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) support for an EAP method can be enabled for EAPHost EAP methods that support the transmission of type-length-value objects (TLVs).</span></span> <span data-ttu-id="729cc-105">Если включена поддержка NAP в аппаратном контроллере, пакеты NAP передаются внутри пакетов методов EAP.</span><span class="sxs-lookup"><span data-stu-id="729cc-105">When in-band NAP support is enabled, NAP packets are transported inside EAP method packets.</span></span>

<span data-ttu-id="729cc-106">В противоположность этому, если включена поддержка нестандартного NAP, Обмен данными [о состоянии работоспособности](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) NAP выполняется через средства, отличные от внутренних для пакетов методов EAP.</span><span class="sxs-lookup"><span data-stu-id="729cc-106">In contrast, when out-of-band NAP support is enabled, the NAP [Statement of Health](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) exchange occurs through means other than internal to EAP method packets.</span></span>

<span data-ttu-id="729cc-107">Все ТЛВС относятся к конкретному поставщику.</span><span class="sxs-lookup"><span data-stu-id="729cc-107">All TLVs are vendor specific.</span></span>

## <a name="implementing-nap-support-on-eap-peer-methods"></a><span data-ttu-id="729cc-108">Реализация поддержки NAP на одноранговых методах EAP</span><span class="sxs-lookup"><span data-stu-id="729cc-108">Implementing NAP Support on EAP Peer Methods</span></span>

<span data-ttu-id="729cc-109">Реализация однорангового метода EAP получает TLV, содержащий TLV запроса [состояния работоспособности](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) от сервера EAP.</span><span class="sxs-lookup"><span data-stu-id="729cc-109">The EAP peer method implementation receives a TLV containing the [Statement of Health](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) request TLV from an EAP server.</span></span>

<span data-ttu-id="729cc-110">Затем реализация однорангового метода EAP передает TLV, содержащий TLV запроса SoH, в EAPHost следующим образом.</span><span class="sxs-lookup"><span data-stu-id="729cc-110">The EAP peer method implementation then passes the TLV containing the SoH request TLV to EAPHost as follows.</span></span>

-   <span data-ttu-id="729cc-111">Реализация однорангового метода EAP возвращает код действия [**еаппирмесодреспонсеактионреспонд**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) в значение EAPHost при возврате из [**еаппирпроцессрекуестпаккет**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).</span><span class="sxs-lookup"><span data-stu-id="729cc-111">The EAP peer method implementation returns the action code [**EapPeerMethodResponseActionRespond**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) to EAPHost on return from [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).</span></span>
-   <span data-ttu-id="729cc-112">EAPHost вызывает [**еаппиржетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) из реализации однорангового метода EAP.</span><span class="sxs-lookup"><span data-stu-id="729cc-112">EAPHost calls [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) from the EAP peer method implementation.</span></span> <span data-ttu-id="729cc-113">Атрибуты передаются в процесс.</span><span class="sxs-lookup"><span data-stu-id="729cc-113">The attributes are passed in the process.</span></span>
-   <span data-ttu-id="729cc-114">Реализация однорангового метода EAP возвращает TLV, содержащий TLV запроса SoH в [**еаппиржетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes).</span><span class="sxs-lookup"><span data-stu-id="729cc-114">The EAP peer method implementation returns the TLV containing the SoH request TLV in [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes).</span></span> <span data-ttu-id="729cc-115">Атрибуты принимаются в процессе.</span><span class="sxs-lookup"><span data-stu-id="729cc-115">The attributes are received in the process.</span></span>

<span data-ttu-id="729cc-116">Реализация однорангового метода EAP получает TLV, содержащий TLV SoH из EAPHost, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="729cc-116">The EAP peer method implementation receives a TLV containing an SoH TLV from EAPHost as follows.</span></span>

-   <span data-ttu-id="729cc-117">EAPHost вызывает [**еаппирсетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) из реализации однорангового метода EAP.</span><span class="sxs-lookup"><span data-stu-id="729cc-117">EAPHost calls [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) from the EAP peer method implementation.</span></span> <span data-ttu-id="729cc-118">**Еаппирсетреспонсеаттрибутес** содержит TLV, в котором находится TLV состояния работоспособности.</span><span class="sxs-lookup"><span data-stu-id="729cc-118">**EapPeerSetResponseAttributes** contains a TLV that houses an SoH TLV.</span></span>
-   <span data-ttu-id="729cc-119">Реализация однорангового метода EAP отправляет TLV SoH на сервер EAP.</span><span class="sxs-lookup"><span data-stu-id="729cc-119">The EAP peer method implementation sends the SoH TLV to the EAP server.</span></span>
-   <span data-ttu-id="729cc-120">Реализация однорангового метода EAP получает TLV, содержащий TLV ответа SoH от сервера EAP.</span><span class="sxs-lookup"><span data-stu-id="729cc-120">The EAP peer method implementation receives a TLV containing an SoH response TLV from the EAP server.</span></span>

<span data-ttu-id="729cc-121">Реализация однорангового метода EAP передает TLV, содержащий TLV ответа SoH, в EAPHost следующим образом.</span><span class="sxs-lookup"><span data-stu-id="729cc-121">The EAP peer method implementation passes the TLV containing the SoH response TLV to EAPHost as follows.</span></span>

-   <span data-ttu-id="729cc-122">Реализация однорангового метода EAP возвращает код действия **еаппирмесодреспонсеактионреспонд** в значение EAPHost при возврате из [**еаппирпроцессрекуестпаккет**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).</span><span class="sxs-lookup"><span data-stu-id="729cc-122">The EAP peer method implementation returns the action code **EapPeerMethodResponseActionRespond** to EAPHost on return from [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).</span></span>
-   <span data-ttu-id="729cc-123">EAPHost вызывает [**еаппиржетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) из реализаций однорангового метода EAP.</span><span class="sxs-lookup"><span data-stu-id="729cc-123">EAPHost calls [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) from the EAP peer method implementations.</span></span> <span data-ttu-id="729cc-124">Структура [**\_ атрибутов EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes) передается в процессе.</span><span class="sxs-lookup"><span data-stu-id="729cc-124">The [**EAP\_ATTRIBUTES**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes) structure is passed in the process.</span></span>
-   <span data-ttu-id="729cc-125">Реализация однорангового метода EAP возвращает TLV, содержащий TLV ответа SoH в [**еаппирсетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes).</span><span class="sxs-lookup"><span data-stu-id="729cc-125">The EAP peer method implementation returns the TLV containing the SoH response TLV in [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes).</span></span>

> [!Note]  
> <span data-ttu-id="729cc-126">Элементу **еаптипе** структуры [**\_ атрибута EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) всегда будет присвоено значение **еатеаптлв** , а элемент **pValue** будет указывать на первый байт TLV, содержащего TLV ответа SoH.</span><span class="sxs-lookup"><span data-stu-id="729cc-126">The **eapType** member of the [**EAP\_ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) structure will always be set to **eatEAPTLV** and the **pValue** member will point to the first byte of the TLV that contains the SoH response TLV.</span></span>

 

### <a name="implementing-nap-support-on-eap-server-methods"></a><span data-ttu-id="729cc-127">Реализация поддержки NAP для методов сервера EAP</span><span class="sxs-lookup"><span data-stu-id="729cc-127">Implementing NAP Support on EAP Server Methods</span></span>

<span data-ttu-id="729cc-128">Реализация метода сервера EAP конструирует TLV, содержащий TLV запроса SoH.</span><span class="sxs-lookup"><span data-stu-id="729cc-128">The EAP server method implementation constructs a TLV containing an SoH request TLV.</span></span> <span data-ttu-id="729cc-129">Реализация метода сервера EAP отправляет этот TLV, содержащий TLV запроса SoH, на узел EAP.</span><span class="sxs-lookup"><span data-stu-id="729cc-129">The EAP server method implementation sends this TLV containing the SoH Request TLV to the EAP peer.</span></span> <span data-ttu-id="729cc-130">Реализация метода сервера EAP получает TLV от узла EAP.</span><span class="sxs-lookup"><span data-stu-id="729cc-130">The EAP server method implementation receives the TLV from the EAP peer.</span></span>

<span data-ttu-id="729cc-131">Реализация метода сервера EAP передает TLV, содержащий TLV SoH, в EAPHost следующим образом.</span><span class="sxs-lookup"><span data-stu-id="729cc-131">The EAP server method implementation passes the TLV containing an SoH TLV to EAPHost as follows.</span></span>

-   <span data-ttu-id="729cc-132">Реализация метода сервера EAP возвращает **\_ ответ на метод \_ проверки подлинности метода \_ EAP \_** для кода действия, реагирующий на EAPHost при возврате из [**еапмесодаусентикаторрецеивепаккет**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket).</span><span class="sxs-lookup"><span data-stu-id="729cc-132">The EAP server method implementation returns the action code **EAP\_METHOD\_AUTHENTICATOR\_RESPONSE\_RESPOND** to EAPHost on return from [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket).</span></span>
-   <span data-ttu-id="729cc-133">EAPHost вызывает [**еапмесодаусентикаторжетаттрибутес**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) из реализации метода сервера EAP.</span><span class="sxs-lookup"><span data-stu-id="729cc-133">EAPHost calls [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) from the EAP server method implementation.</span></span>
-   <span data-ttu-id="729cc-134">Реализация метода сервера EAP возвращает TLV, содержащий TLV SoH в [**еапмесодаусентикаторжетаттрибутес**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes).</span><span class="sxs-lookup"><span data-stu-id="729cc-134">The EAP server method implementation returns the TLV containing the SoH TLV in [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes).</span></span>

<span data-ttu-id="729cc-135">Реализация метода сервера EAP получает TLV, содержащий TLV ответа SoH из EAPHost, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="729cc-135">The EAP server method implementation receives a TLV containing an SoH response TLV from EAPHost as follows.</span></span>

-   <span data-ttu-id="729cc-136">EAPHost вызывает [**еапмесодаусентикаторсетаттрибутес**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) из реализации метода сервера EAP.</span><span class="sxs-lookup"><span data-stu-id="729cc-136">EAPHost calls [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) from the EAP server method implementation.</span></span>
-   <span data-ttu-id="729cc-137">TLV, содержащий TLV ответа SoH, возвращается в [ **еапмесодаусентикаторсетаттрибутес**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)</span><span class="sxs-lookup"><span data-stu-id="729cc-137">The TLV containing the SoH response TLV is returned in [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)</span></span>
-   <span data-ttu-id="729cc-138">Реализация метода сервера EAP отправляет TLV, содержащий TLV ответа SoH.</span><span class="sxs-lookup"><span data-stu-id="729cc-138">The EAP server method implementation sends the TLV containing the SoH response TLV.</span></span>

> [!Note]  
> <span data-ttu-id="729cc-139">Элементу **еаптипе** структуры [**\_ атрибута EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) всегда будет присвоено значение **еатеаптлв** , а элемент **pValue** будет указывать на первый байт TLV, содержащего TLV ответа SoH.</span><span class="sxs-lookup"><span data-stu-id="729cc-139">The **eapType** member of the [**EAP\_ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) structure will always be set to **eatEAPTLV** and the **pValue** member will point to the first byte of the TLV that contains the SoH response TLV.</span></span>

 

### <a name="messages"></a><span data-ttu-id="729cc-140">Сообщения</span><span class="sxs-lookup"><span data-stu-id="729cc-140">Messages</span></span>

<span data-ttu-id="729cc-141">TLV состояния работоспособности EAP используется для инкапсуляции протокола SoH для передачи с помощью метода EAP.</span><span class="sxs-lookup"><span data-stu-id="729cc-141">The EAP SoH TLV is used to encapsulate the SoH protocol for transmission via an EAP method.</span></span> <span data-ttu-id="729cc-142">Все ТЛВС состояния работоспособности EAP имеют одинаковую структуру, отличающуюся только ИДЕНТИФИКАТОРом сообщения и частью данных сообщения.</span><span class="sxs-lookup"><span data-stu-id="729cc-142">All EAP SoH TLVs have the same structure, differing only on the message ID and data portion of the message.</span></span>

<span data-ttu-id="729cc-143">Дополнительные сведения см. в статье [уведомление о состоянии работоспособности защиты доступа к сети (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83918).</span><span class="sxs-lookup"><span data-stu-id="729cc-143">For more information, see [Network Access Protection (NAP) Statement of Health (SoH) Messages](https://go.microsoft.com/fwlink/p/?linkid=83918).</span></span>

## <a name="related-topics"></a><span data-ttu-id="729cc-144">См. также</span><span class="sxs-lookup"><span data-stu-id="729cc-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="729cc-145">Настройка пользовательского интерфейса метода EAP</span><span class="sxs-lookup"><span data-stu-id="729cc-145">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="729cc-146">Включение групповая политика</span><span class="sxs-lookup"><span data-stu-id="729cc-146">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="729cc-147">Реализация поддержки NAP для методов EAP</span><span class="sxs-lookup"><span data-stu-id="729cc-147">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="729cc-148">Передача данных между запрашивающим и методами EAP</span><span class="sxs-lookup"><span data-stu-id="729cc-148">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="729cc-149">EAPHost отправителей запросов</span><span class="sxs-lookup"><span data-stu-id="729cc-149">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 