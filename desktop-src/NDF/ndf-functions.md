---
title: Функции NDF
description: Следующие функции позволяют разработчикам программного обеспечения использовать функциональные возможности, предоставляемые инфраструктурой диагностики сети (NDF).
ms.assetid: c2774e05-82f4-4d40-a80c-ad773bb03ca7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a039768b77d69072111f814cb871115bcca24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672049"
---
# <a name="ndf-functions"></a><span data-ttu-id="2cc66-103">Функции NDF</span><span class="sxs-lookup"><span data-stu-id="2cc66-103">NDF Functions</span></span>

<span data-ttu-id="2cc66-104">Следующие функции позволяют разработчикам программного обеспечения использовать функциональные возможности, предоставляемые инфраструктурой диагностики сети (NDF).</span><span class="sxs-lookup"><span data-stu-id="2cc66-104">The following functions enable software developers to use the functionality provided by the Network Diagnostic Framework (NDF).</span></span> <span data-ttu-id="2cc66-105">При возникновении проблем в сети NDF может диагностировать основную причину и корректно обработать необходимое разрешение, иногда даже выполняя необходимые исправления.</span><span class="sxs-lookup"><span data-stu-id="2cc66-105">When network issues occur, NDF can diagnose the root cause and handle the necessary resolution gracefully, sometimes even performing the necessary repairs.</span></span>

> [!Note]  
> <span data-ttu-id="2cc66-106">Эти функции предназначены для разработчиков, реализующих базовую функциональность NDF в своих приложениях.</span><span class="sxs-lookup"><span data-stu-id="2cc66-106">These functions are for developers implementing basic NDF functionality in their applications.</span></span>

 

-   [<span data-ttu-id="2cc66-107">**копихелператтрибуте**</span><span class="sxs-lookup"><span data-stu-id="2cc66-107">**CopyHelperAttribute**</span></span>](copyhelperattribute.md)
-   [<span data-ttu-id="2cc66-108">**копирепаиринфо**</span><span class="sxs-lookup"><span data-stu-id="2cc66-108">**CopyRepairInfo**</span></span>](copyrepairinfo.md)
-   [<span data-ttu-id="2cc66-109">**копируткаусеинфо**</span><span class="sxs-lookup"><span data-stu-id="2cc66-109">**CopyRootCauseInfo**</span></span>](copyrootcauseinfo.md)
-   [<span data-ttu-id="2cc66-110">**фрирепаиринфоексс**</span><span class="sxs-lookup"><span data-stu-id="2cc66-110">**FreeRepairInfoExs**</span></span>](freerepairinfoexs.md)
-   [<span data-ttu-id="2cc66-111">**фрирепаиринфос**</span><span class="sxs-lookup"><span data-stu-id="2cc66-111">**FreeRepairInfos**</span></span>](freerepairinfos.md)
-   [<span data-ttu-id="2cc66-112">**фрируткаусеинфос**</span><span class="sxs-lookup"><span data-stu-id="2cc66-112">**FreeRootCauseInfos**</span></span>](freerootcauseinfos.md)
-   [<span data-ttu-id="2cc66-113">**фрихелператтрибутес**</span><span class="sxs-lookup"><span data-stu-id="2cc66-113">**FreeHelperAttributes**</span></span>](freehelperattributes.md)
-   [<span data-ttu-id="2cc66-114">**фриуиинфо**</span><span class="sxs-lookup"><span data-stu-id="2cc66-114">**FreeUiInfo**</span></span>](freeuiinfo.md)
-   [<span data-ttu-id="2cc66-115">**ндфканцелинЦидент**</span><span class="sxs-lookup"><span data-stu-id="2cc66-115">**NdfCancelIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcancelincident)
-   [<span data-ttu-id="2cc66-116">**ндфклосеинЦидент**</span><span class="sxs-lookup"><span data-stu-id="2cc66-116">**NdfCloseIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
-   [<span data-ttu-id="2cc66-117">**ндфкреатеконнективитинЦидент**</span><span class="sxs-lookup"><span data-stu-id="2cc66-117">**NdfCreateConnectivityIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateconnectivityincident)
-   [<span data-ttu-id="2cc66-118">**ндфкреатеднсинЦидент**</span><span class="sxs-lookup"><span data-stu-id="2cc66-118">**NdfCreateDNSIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident)
-   [<span data-ttu-id="2cc66-119">**ндфкреатеграупингинЦидент**</span><span class="sxs-lookup"><span data-stu-id="2cc66-119">**NdfCreateGroupingIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreategroupingincident)
-   [<span data-ttu-id="2cc66-120">**ндфкреатеинбаундинЦидент**</span><span class="sxs-lookup"><span data-stu-id="2cc66-120">**NdfCreateInboundIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateinboundincident)
-   [<span data-ttu-id="2cc66-121">**ндфкреатеинЦидент**</span><span class="sxs-lookup"><span data-stu-id="2cc66-121">**NdfCreateIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateincident)
-   [<span data-ttu-id="2cc66-122">**ндфкреатенетконнектионинЦидент**</span><span class="sxs-lookup"><span data-stu-id="2cc66-122">**NdfCreateNetConnectionIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatenetconnectionincident)
-   [<span data-ttu-id="2cc66-123">**ндфкреатепнрпинЦидент**</span><span class="sxs-lookup"><span data-stu-id="2cc66-123">**NdfCreatePnrpIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatepnrpincident)
-   [<span data-ttu-id="2cc66-124">**ндфкреатешарингинЦидент**</span><span class="sxs-lookup"><span data-stu-id="2cc66-124">**NdfCreateSharingIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatesharingincident)
-   [<span data-ttu-id="2cc66-125">**ндфкреатевебинЦидент**</span><span class="sxs-lookup"><span data-stu-id="2cc66-125">**NdfCreateWebIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
-   [<span data-ttu-id="2cc66-126">**ндфкреатевебинЦидентекс**</span><span class="sxs-lookup"><span data-stu-id="2cc66-126">**NdfCreateWebIncidentEx**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincidentex)
-   [<span data-ttu-id="2cc66-127">**ндфкреатевинсоккинЦидент**</span><span class="sxs-lookup"><span data-stu-id="2cc66-127">**NdfCreateWinSockIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident)
-   [<span data-ttu-id="2cc66-128">**ндфдиагносеинЦидент**</span><span class="sxs-lookup"><span data-stu-id="2cc66-128">**NdfDiagnoseIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident)
-   [<span data-ttu-id="2cc66-129">**ндфексекутедиагносис**</span><span class="sxs-lookup"><span data-stu-id="2cc66-129">**NdfExecuteDiagnosis**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
-   [<span data-ttu-id="2cc66-130">**ндфжеттрацефиле**</span><span class="sxs-lookup"><span data-stu-id="2cc66-130">**NdfGetTraceFile**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfgettracefile)
-   [<span data-ttu-id="2cc66-131">**ндфрепаиринЦидент**</span><span class="sxs-lookup"><span data-stu-id="2cc66-131">**NdfRepairIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident)
-   [<span data-ttu-id="2cc66-132">**утилассемблестрингсвисаллок**</span><span class="sxs-lookup"><span data-stu-id="2cc66-132">**UtilAssembleStringsWithAlloc**</span></span>](utilassemblestringswithalloc.md)
-   [<span data-ttu-id="2cc66-133">**утиллоадстрингвисаллок**</span><span class="sxs-lookup"><span data-stu-id="2cc66-133">**UtilLoadStringWithAlloc**</span></span>](utilloadstringwithalloc.md)
-   [<span data-ttu-id="2cc66-134">**утилстрингкопивисаллок**</span><span class="sxs-lookup"><span data-stu-id="2cc66-134">**UtilStringCopyWithAlloc**</span></span>](utilstringcopywithalloc.md)

 

 




