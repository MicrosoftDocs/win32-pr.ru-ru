---
title: Атрибуты EAP
description: — Это \_ Структура атрибута EAP, которая содержит предварительно определенный тип данных, связанных с сеансом проверки подлинности.
ms.assetid: 3c54cca2-cd3b-4149-bb0e-036d490cdd3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5348ee300c0e4d07d6aaf110ba9074b1ac32c02a
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "105710409"
---
# <a name="eap-attributes"></a><span data-ttu-id="d135e-103">Атрибуты EAP</span><span class="sxs-lookup"><span data-stu-id="d135e-103">EAP Attributes</span></span>

<span data-ttu-id="d135e-104">Атрибут EAP — это структура [**\_ атрибута EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) , которая содержит предварительно определенный тип данных, связанных с сеансом проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="d135e-104">An EAP attribute is an [**EAP\_ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) structure that contains a predetermined type of data relating to an authentication session.</span></span> <span data-ttu-id="d135e-105">Атрибуты используются для обмена данными между методами EAP и отправителей запросов или между методами и проверками подлинности EAP.</span><span class="sxs-lookup"><span data-stu-id="d135e-105">Attributes are used to communicate information between EAP methods and supplicants or between EAP methods and authenticators.</span></span> <span data-ttu-id="d135e-106">Реализации метода EAP в одноранговых сетях и средствах проверки подлинности могут обмениваться этими атрибутами по сети.</span><span class="sxs-lookup"><span data-stu-id="d135e-106">Peer and authenticator implementations of an EAP method may exchange these attributes over a network.</span></span>

<span data-ttu-id="d135e-107">Полный список поддерживаемых типов атрибутов представлен в разделе [**\_ \_ тип атрибута EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span><span class="sxs-lookup"><span data-stu-id="d135e-107">A complete list of supported attribute types appears in the topic [**EAP\_ATTRIBUTE\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span></span>

## <a name="attributes-consumed-by-supplicants"></a><span data-ttu-id="d135e-108">Атрибуты, используемые отправителей запросов</span><span class="sxs-lookup"><span data-stu-id="d135e-108">Attributes Consumed by Supplicants</span></span>

<span data-ttu-id="d135e-109">Следующие типы атрибутов используются 802.1 X отправителей запросов.</span><span class="sxs-lookup"><span data-stu-id="d135e-109">The following attribute types are consumed by 802.1X supplicants.</span></span>

-   <span data-ttu-id="d135e-110">**еатвендорспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="d135e-110">**eatVendorSpecific**</span></span>

<span data-ttu-id="d135e-111">Следующие типы атрибутов используются PPP Client отправителей запросов.</span><span class="sxs-lookup"><span data-stu-id="d135e-111">The following attribute types are consumed by PPP client supplicants.</span></span>

-   <span data-ttu-id="d135e-112">**еатминимум**</span><span class="sxs-lookup"><span data-stu-id="d135e-112">**eatMinimum**</span></span>
-   <span data-ttu-id="d135e-113">**еатеаптлв**</span><span class="sxs-lookup"><span data-stu-id="d135e-113">**eatEAPTLV**</span></span>

<span data-ttu-id="d135e-114">Следующие типы атрибутов используются PPP Server отправителей запросов.</span><span class="sxs-lookup"><span data-stu-id="d135e-114">The following attribute types are consumed by PPP server supplicants.</span></span>

-   <span data-ttu-id="d135e-115">**еатусернаме**</span><span class="sxs-lookup"><span data-stu-id="d135e-115">**eatUserName**</span></span>
-   <span data-ttu-id="d135e-116">**еатреплимессаже**</span><span class="sxs-lookup"><span data-stu-id="d135e-116">**eatReplyMessage**</span></span>
-   <span data-ttu-id="d135e-117">**еатстате**</span><span class="sxs-lookup"><span data-stu-id="d135e-117">**eatState**</span></span>
-   <span data-ttu-id="d135e-118">**еатсессионтимеаут**</span><span class="sxs-lookup"><span data-stu-id="d135e-118">**eatSessionTimeout**</span></span>
-   <span data-ttu-id="d135e-119">**еатеапмессаже**</span><span class="sxs-lookup"><span data-stu-id="d135e-119">**eatEAPMessage**</span></span>

## <a name="attributes-exported-by-methods"></a><span data-ttu-id="d135e-120">Атрибуты, экспортированные методами</span><span class="sxs-lookup"><span data-stu-id="d135e-120">Attributes Exported by Methods</span></span>

<span data-ttu-id="d135e-121">Методы EAP могут экспортировать следующие типы атрибутов.</span><span class="sxs-lookup"><span data-stu-id="d135e-121">The following attribute types could be exported by EAP methods.</span></span>

-   <span data-ttu-id="d135e-122">**еатклеартекстпассворд**</span><span class="sxs-lookup"><span data-stu-id="d135e-122">**eatClearTextPassword**</span></span>
-   <span data-ttu-id="d135e-123">**еаткуарантинесох**</span><span class="sxs-lookup"><span data-stu-id="d135e-123">**eatQuarantineSoH**</span></span>
-   <span data-ttu-id="d135e-124">**еатмесодид**</span><span class="sxs-lookup"><span data-stu-id="d135e-124">**eatMethodId**</span></span>

<span data-ttu-id="d135e-125">Следующий тип атрибута экспортируется методами [TLS](/previous-versions/windows/embedded/ms885336(v=msdn.10)) (EAP-TLS) протокола EAP.</span><span class="sxs-lookup"><span data-stu-id="d135e-125">The following attribute type is exported by EAP [Transport Level Security (TLS)](/previous-versions/windows/embedded/ms885336(v=msdn.10)) (EAP-TLS) methods.</span></span>

-   <span data-ttu-id="d135e-126">**еатцертификатеоид**</span><span class="sxs-lookup"><span data-stu-id="d135e-126">**eatCertificateOID**</span></span>

<span data-ttu-id="d135e-127">Следующие типы атрибутов экспортируются методами [протокола проверки подлинности Microsoft Challenge](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (MS-CHAPv2) версии 2,0.</span><span class="sxs-lookup"><span data-stu-id="d135e-127">The following attribute types are exported by [Microsoft Challenge Handshake Authentication Protocol version 2.0](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (MS-CHAPv2) methods.</span></span>

-   <span data-ttu-id="d135e-128">**еатусернаме**</span><span class="sxs-lookup"><span data-stu-id="d135e-128">**eatUserName**</span></span>
-   <span data-ttu-id="d135e-129">**еаткредентиалсчанжед**</span><span class="sxs-lookup"><span data-stu-id="d135e-129">**eatCredentialsChanged**</span></span>

<span data-ttu-id="d135e-130">Сервер политики сети (NPS) использует следующий тип атрибута.</span><span class="sxs-lookup"><span data-stu-id="d135e-130">The following attribute type is consumed by Network Policy Server (NPS).</span></span>

-   <span data-ttu-id="d135e-131">**еатцертификатеоид**</span><span class="sxs-lookup"><span data-stu-id="d135e-131">**eatCertificateOID**</span></span>

<span data-ttu-id="d135e-132">Следующие типы атрибутов экспортируются с помощью методов [протокола PEAP](/previous-versions/windows/embedded/ms899190(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="d135e-132">The following attribute types are exported by [Protected Extensible Authentication Protocol (PEAP)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) methods.</span></span>

-   <span data-ttu-id="d135e-133">**еатусернаме**</span><span class="sxs-lookup"><span data-stu-id="d135e-133">**eatUserName**</span></span>
-   <span data-ttu-id="d135e-134">**еатпеапембеддедеаптипеид**</span><span class="sxs-lookup"><span data-stu-id="d135e-134">**eatPEAPEmbeddedEAPTypeId**</span></span>
-   <span data-ttu-id="d135e-135">**еатпеапфастроамедсессион**</span><span class="sxs-lookup"><span data-stu-id="d135e-135">**eatPEAPFastRoamedSession**</span></span>
-   <span data-ttu-id="d135e-136">**еаткуарантинесох**</span><span class="sxs-lookup"><span data-stu-id="d135e-136">**eatQuarantineSoH**</span></span>

## <a name="related-topics"></a><span data-ttu-id="d135e-137">См. также</span><span class="sxs-lookup"><span data-stu-id="d135e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d135e-138">**\_атрибут EAP**</span><span class="sxs-lookup"><span data-stu-id="d135e-138">**EAP\_ATTRIBUTE**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)
</dt> <dt>

[<span data-ttu-id="d135e-139">**\_тип атрибута \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="d135e-139">**EAP\_ATTRIBUTE\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
</dt> </dl>

 

 