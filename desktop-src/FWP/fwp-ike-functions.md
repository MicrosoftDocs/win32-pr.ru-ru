---
title: Функции IKE/AuthIP
description: (WFP), используемые для взаимодействия с модулями ключей \ 8212; протокол IKE (IKE), протокол IKE v2 (IKEv2) и протоколом AuthIP (проверка подлинности в Интернете).
ms.assetid: df36b6cc-a304-4426-8f16-1bf92fd721e1
keywords:
- Функции протокол IKE API платформы фильтрации Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cce5d3e2393bb1a83ebf816375f537318bb4b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331027"
---
# <a name="ikeauthip-functions"></a><span data-ttu-id="ef418-104">Функции IKE/AuthIP</span><span class="sxs-lookup"><span data-stu-id="ef418-104">IKE/AuthIP Functions</span></span>

<span data-ttu-id="ef418-105">Функции платформы фильтрации Windows (WFP), используемые для взаимодействия с модулями ключей: протокол IKE (IKE), протокол IKE v2 (IKEv2) и протокол IP с проверкой подлинности (AuthIP), приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="ef418-105">The Windows Filtering Platform (WFP) functions used to interact with keying modules—Internet Key Exchange (IKE), Internet Key Exchange v2 (IKEv2), and Authenticated Internet Protocol (AuthIP)—are as follows.</span></span>

-   <span data-ttu-id="ef418-106">Икикстжетстатистикс:</span><span class="sxs-lookup"><span data-stu-id="ef418-106">IkeextGetStatistics:</span></span>
    -   <span data-ttu-id="ef418-107">[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="ef418-107">[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0) (Windows Vista)</span></span>
    -   <span data-ttu-id="ef418-108">[**IkeextGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics1) (Windows 7 и более поздние версии)</span><span class="sxs-lookup"><span data-stu-id="ef418-108">[**IkeextGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="ef418-109">**IkeextSaCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="ef418-109">**IkeextSaCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)
-   [<span data-ttu-id="ef418-110">**IkeextSaDbGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="ef418-110">**IkeextSaDbGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadbgetsecurityinfo0)
-   [<span data-ttu-id="ef418-111">**IkeextSaDbSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="ef418-111">**IkeextSaDbSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadbsetsecurityinfo0)
-   [<span data-ttu-id="ef418-112">**IkeextSaDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="ef418-112">**IkeextSaDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)
-   [<span data-ttu-id="ef418-113">**IkeextSaDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="ef418-113">**IkeextSaDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadestroyenumhandle0)
-   <span data-ttu-id="ef418-114">Икикстсаенум:</span><span class="sxs-lookup"><span data-stu-id="ef418-114">IkeextSaEnum:</span></span>
    -   <span data-ttu-id="ef418-115">[**IkeextSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="ef418-115">[**IkeextSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum0) (Windows Vista)</span></span>
    -   <span data-ttu-id="ef418-116">[**IkeextSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="ef418-116">[**IkeextSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum1) (Windows 7)</span></span>
    -   <span data-ttu-id="ef418-117">[**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="ef418-117">[**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2) (Windows 8)</span></span>
-   <span data-ttu-id="ef418-118">Икикстсажетбид:</span><span class="sxs-lookup"><span data-stu-id="ef418-118">IkeextSaGetById:</span></span>
    -   <span data-ttu-id="ef418-119">[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="ef418-119">[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0) (Windows Vista)</span></span>
    -   <span data-ttu-id="ef418-120">[**IkeextSaGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="ef418-120">[**IkeextSaGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid1) (Windows 7)</span></span>
    -   <span data-ttu-id="ef418-121">[**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="ef418-121">[**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2) (Windows 8)</span></span>

 

 




