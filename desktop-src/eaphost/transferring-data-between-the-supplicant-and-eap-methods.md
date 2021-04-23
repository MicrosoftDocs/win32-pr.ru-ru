---
title: Передача данных между запрашивающим и методами EAP
description: Сведения о передаче данных между запрашивающим и методами EAP. Передача данных между методами выполняется с помощью атрибутов EAP.
ms.assetid: f1bcff61-286a-4f18-8a5d-93d5d1fd2b5b
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187858347e8630bfbaba0683700eaa39f116f6ce
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413753"
---
# <a name="transferring-data-between-the-supplicant-and-eap-methods"></a><span data-ttu-id="0c0f6-104">Передача данных между запрашивающим и методами EAP</span><span class="sxs-lookup"><span data-stu-id="0c0f6-104">Transferring Data Between the Supplicant and EAP Methods</span></span>

<span data-ttu-id="0c0f6-105">Использование атрибутов EAP позволяет обмениваться данными между отправителей запросов и методами EAP.</span><span class="sxs-lookup"><span data-stu-id="0c0f6-105">Using EAP attributes allows data to be exchanged between supplicants and EAP methods.</span></span>

## <a name="attribute-consumption"></a><span data-ttu-id="0c0f6-106">Использование атрибута</span><span class="sxs-lookup"><span data-stu-id="0c0f6-106">Attribute Consumption</span></span>

<span data-ttu-id="0c0f6-107">[**Еафостпирбегинсессион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) использует атрибуты EAP, которые передаются непосредственно в настроенный метод EAP.</span><span class="sxs-lookup"><span data-stu-id="0c0f6-107">[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) consumes EAP attributes that are passed directly to the configured EAP method.</span></span> <span data-ttu-id="0c0f6-108">Аналогичным образом методы EAP могут возвращать код действия, указывающий на то, что атрибуты доступны и должны собираются атрибуты с помощью [**еафостпиржетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).</span><span class="sxs-lookup"><span data-stu-id="0c0f6-108">Similarly, EAP methods are free to return an action code that indicates to the supplicant that attributes are available and that it should collect the attributes using [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).</span></span>

<span data-ttu-id="0c0f6-109">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="0c0f6-109">For more information, see the following topics.</span></span>

-   <span data-ttu-id="0c0f6-110">[Коды действий запрашивающих сторон EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span><span class="sxs-lookup"><span data-stu-id="0c0f6-110">[EAP Peer Supplicant Action Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span></span>
-   <span data-ttu-id="0c0f6-111">[Коды причин однорангового запрашивающего устройства EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).</span><span class="sxs-lookup"><span data-stu-id="0c0f6-111">[EAP Peer Supplicant Reason Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).</span></span>
-   <span data-ttu-id="0c0f6-112">[Коды действий методов средства проверки подлинности EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).</span><span class="sxs-lookup"><span data-stu-id="0c0f6-112">[EAP Authenticator Method Action Codes](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).</span></span>

<span data-ttu-id="0c0f6-113">Отправителей запросов должны игнорировать атрибуты, которые они не распознают или не могут работать с ними.</span><span class="sxs-lookup"><span data-stu-id="0c0f6-113">Supplicants are expected to ignore attributes that they do not recognize or cannot act upon.</span></span> <span data-ttu-id="0c0f6-114">При использовании [**еафостпирсетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) эти игнорируемые атрибуты отправляются обратно в EAPHost и метод EAP.</span><span class="sxs-lookup"><span data-stu-id="0c0f6-114">Using [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) these ignored attributes are sent back to EAPHost and the EAP method.</span></span>

## <a name="vendor-specific-attributes"></a><span data-ttu-id="0c0f6-115">Атрибуты, зависящие от поставщика</span><span class="sxs-lookup"><span data-stu-id="0c0f6-115">Vendor Specific Attributes</span></span>

<span data-ttu-id="0c0f6-116">С помощью атрибута EAP, зависящего от поставщика, методы EAP и отправителей запросов могут участвовать в обмене данными с конкретной целью.</span><span class="sxs-lookup"><span data-stu-id="0c0f6-116">By using the vendor-specific EAP attribute, EAP methods and supplicants can engage in data exchange for a specific purpose.</span></span> <span data-ttu-id="0c0f6-117">Атрибуты, зависящие от поставщика, игнорируются отправителей запросов и методами, которые не поддерживают атрибут, зависящий от поставщика.</span><span class="sxs-lookup"><span data-stu-id="0c0f6-117">Vendor-specific attributes are ignored by supplicants and methods that do not support the vendor-specific attribute.</span></span>

<span data-ttu-id="0c0f6-118">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="0c0f6-118">For more information, see the following topics.</span></span>

-   <span data-ttu-id="0c0f6-119">[Атрибуты EAP](about-eap-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="0c0f6-119">[EAP Attributes](about-eap-attributes.md).</span></span>
-   <span data-ttu-id="0c0f6-120">[**Протокол EAP \_ \_тип атрибута**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span><span class="sxs-lookup"><span data-stu-id="0c0f6-120">[**EAP\_ATTRIBUTE\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c0f6-121">См. также</span><span class="sxs-lookup"><span data-stu-id="0c0f6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c0f6-122">Настройка пользовательского интерфейса метода EAP</span><span class="sxs-lookup"><span data-stu-id="0c0f6-122">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="0c0f6-123">Включение групповая политика</span><span class="sxs-lookup"><span data-stu-id="0c0f6-123">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="0c0f6-124">Реализация поддержки NAP In-Band для методов EAP</span><span class="sxs-lookup"><span data-stu-id="0c0f6-124">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="0c0f6-125">Реализация поддержки NAP для методов EAP</span><span class="sxs-lookup"><span data-stu-id="0c0f6-125">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="0c0f6-126">EAPHost отправителей запросов</span><span class="sxs-lookup"><span data-stu-id="0c0f6-126">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




