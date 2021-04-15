---
title: Методы использованием метода ibackgroundcopyjob (BITS)
description: Интерфейс использованием метода ibackgroundcopyjob предоставляет следующие методы. | Методы использованием метода ibackgroundcopyjob (BITS)
ms.assetid: CB1C6D64-416A-4F31-AC9D-B3C1A6818034
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a7ebeeefa90c90435f1294d78c4816cf77be3c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547527"
---
# <a name="ibackgroundcopyjob-methods-bits"></a><span data-ttu-id="51776-104">Методы использованием метода ibackgroundcopyjob (BITS)</span><span class="sxs-lookup"><span data-stu-id="51776-104">IBackgroundCopyJob Methods (BITS)</span></span>

<span data-ttu-id="51776-105">Интерфейс [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="51776-105">The [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="51776-106">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="51776-106">In this section</span></span>

-   [<span data-ttu-id="51776-107">**Метод AddFile**</span><span class="sxs-lookup"><span data-stu-id="51776-107">**AddFile Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)
-   [<span data-ttu-id="51776-108">**Метод Аддфилесет**</span><span class="sxs-lookup"><span data-stu-id="51776-108">**AddFileSet Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)
-   [<span data-ttu-id="51776-109">**Метод Cancel**</span><span class="sxs-lookup"><span data-stu-id="51776-109">**Cancel Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel)
-   [<span data-ttu-id="51776-110">**Метод Complete**</span><span class="sxs-lookup"><span data-stu-id="51776-110">**Complete Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)
-   [<span data-ttu-id="51776-111">**Метод EnumFiles**</span><span class="sxs-lookup"><span data-stu-id="51776-111">**EnumFiles Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles)
-   [<span data-ttu-id="51776-112">**Метод GetDescription**</span><span class="sxs-lookup"><span data-stu-id="51776-112">**GetDescription Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdescription)
-   [<span data-ttu-id="51776-113">**Метод GetDisplayName**</span><span class="sxs-lookup"><span data-stu-id="51776-113">**GetDisplayName Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdisplayname)
-   [<span data-ttu-id="51776-114">**Метод метода с ошибками**</span><span class="sxs-lookup"><span data-stu-id="51776-114">**GetError Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror)
-   [<span data-ttu-id="51776-115">**Метод Жетерроркаунт**</span><span class="sxs-lookup"><span data-stu-id="51776-115">**GetErrorCount Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterrorcount)
-   [<span data-ttu-id="51776-116">**Метод GetId**</span><span class="sxs-lookup"><span data-stu-id="51776-116">**GetId Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getid)
-   [<span data-ttu-id="51776-117">**Метод Жетминимумретриделай**</span><span class="sxs-lookup"><span data-stu-id="51776-117">**GetMinimumRetryDelay Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getminimumretrydelay)
-   [<span data-ttu-id="51776-118">**Метод Жетнопрогресстимеаут**</span><span class="sxs-lookup"><span data-stu-id="51776-118">**GetNoProgressTimeout Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnoprogresstimeout)
-   [<span data-ttu-id="51776-119">**Метод Жетнотифифлагс**</span><span class="sxs-lookup"><span data-stu-id="51776-119">**GetNotifyFlags Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnotifyflags)
-   [<span data-ttu-id="51776-120">**Метод Жетнотифинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="51776-120">**GetNotifyInterface Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnotifyinterface)
-   [<span data-ttu-id="51776-121">**Метод, являющийся владельцем**</span><span class="sxs-lookup"><span data-stu-id="51776-121">**GetOwner Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getowner)
-   [<span data-ttu-id="51776-122">**Метод GetPriority**</span><span class="sxs-lookup"><span data-stu-id="51776-122">**GetPriority Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getpriority)
-   [<span data-ttu-id="51776-123">**Метод Progress**</span><span class="sxs-lookup"><span data-stu-id="51776-123">**GetProgress Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress)
-   [<span data-ttu-id="51776-124">**Метод Жетпроксисеттингс**</span><span class="sxs-lookup"><span data-stu-id="51776-124">**GetProxySettings Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getproxysettings)
-   [<span data-ttu-id="51776-125">**Метод WebMethod**</span><span class="sxs-lookup"><span data-stu-id="51776-125">**GetState Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate)
-   [<span data-ttu-id="51776-126">**Метод со временем**</span><span class="sxs-lookup"><span data-stu-id="51776-126">**GetTimes Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-gettimes)
-   [<span data-ttu-id="51776-127">**Метод GetType**</span><span class="sxs-lookup"><span data-stu-id="51776-127">**GetType Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-gettype)
-   [<span data-ttu-id="51776-128">**Метод Resume**</span><span class="sxs-lookup"><span data-stu-id="51776-128">**Resume Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
-   [<span data-ttu-id="51776-129">**Метод SetDescription**</span><span class="sxs-lookup"><span data-stu-id="51776-129">**SetDescription Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setdescription)
-   [<span data-ttu-id="51776-130">**Метод Сетдисплайнаме**</span><span class="sxs-lookup"><span data-stu-id="51776-130">**SetDisplayName Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setdisplayname)
-   [<span data-ttu-id="51776-131">**Метод Сетминимумретриделай**</span><span class="sxs-lookup"><span data-stu-id="51776-131">**SetMinimumRetryDelay Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay)
-   [<span data-ttu-id="51776-132">**Метод Сетнопрогресстимеаут**</span><span class="sxs-lookup"><span data-stu-id="51776-132">**SetNoProgressTimeout Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout)
-   [<span data-ttu-id="51776-133">**Метод Сетнотифифлагс**</span><span class="sxs-lookup"><span data-stu-id="51776-133">**SetNotifyFlags Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)
-   [<span data-ttu-id="51776-134">**Метод Сетнотифинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="51776-134">**SetNotifyInterface Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface)
-   [<span data-ttu-id="51776-135">**Метод SetPriority**</span><span class="sxs-lookup"><span data-stu-id="51776-135">**SetPriority Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setpriority)
-   [<span data-ttu-id="51776-136">**Метод SetProxySettings**</span><span class="sxs-lookup"><span data-stu-id="51776-136">**SetProxySettings Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings)
-   [<span data-ttu-id="51776-137">**Метод Suspend**</span><span class="sxs-lookup"><span data-stu-id="51776-137">**Suspend Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend)
-   [<span data-ttu-id="51776-138">**Метод Такеовнершип**</span><span class="sxs-lookup"><span data-stu-id="51776-138">**TakeOwnership Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership)

 

 




