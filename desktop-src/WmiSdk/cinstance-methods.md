---
description: Класс CInstance предоставляет следующие методы.
ms.assetid: B9846350-405D-440E-AC35-16446D3F03F5
ms.tgt_platform: multiple
title: Методы CInstance
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e088f4604263d3fd1673982e22e2f6c88f991b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911519"
---
# <a name="cinstance-methods"></a><span data-ttu-id="29858-103">Методы CInstance</span><span class="sxs-lookup"><span data-stu-id="29858-103">CInstance Methods</span></span>

<span data-ttu-id="29858-104">\[Класс [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="29858-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="29858-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="29858-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="29858-106">Класс [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="29858-106">The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="29858-107">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="29858-107">In this section</span></span>

-   [<span data-ttu-id="29858-108">**Метод Commit**</span><span class="sxs-lookup"><span data-stu-id="29858-108">**Commit method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-commit)
-   [<span data-ttu-id="29858-109">**Методического bool**</span><span class="sxs-lookup"><span data-stu-id="29858-109">**Getbool method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getbool)
-   [<span data-ttu-id="29858-110">**Метод Byte**</span><span class="sxs-lookup"><span data-stu-id="29858-110">**GetByte method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getbyte)
-   [<span data-ttu-id="29858-111">**Метод Жетчстринг**</span><span class="sxs-lookup"><span data-stu-id="29858-111">**GetCHString method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getchstring)
-   [<span data-ttu-id="29858-112">**Метод Жетклассобжектинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="29858-112">**GetClassObjectInterface method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getclassobjectinterface)
-   [<span data-ttu-id="29858-113">**Метод DateTime**</span><span class="sxs-lookup"><span data-stu-id="29858-113">**GetDateTime method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getdatetime)
-   [<span data-ttu-id="29858-114">**Метод DOUBLE**</span><span class="sxs-lookup"><span data-stu-id="29858-114">**GetDOUBLE method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getdouble)
-   [<span data-ttu-id="29858-115">**Метод DWORD**</span><span class="sxs-lookup"><span data-stu-id="29858-115">**GetDWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getdword)
-   [<span data-ttu-id="29858-116">**Метод Жетембеддедобжект**</span><span class="sxs-lookup"><span data-stu-id="29858-116">**GetEmbeddedObject method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getembeddedobject)
-   [<span data-ttu-id="29858-117">**Метод Жетмесодконтекст**</span><span class="sxs-lookup"><span data-stu-id="29858-117">**GetMethodContext method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getmethodcontext)
-   [<span data-ttu-id="29858-118">**Метод GetStatus**</span><span class="sxs-lookup"><span data-stu-id="29858-118">**GetStatus method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getstatus)
-   [<span data-ttu-id="29858-119">**Метод Жетстрингаррай**</span><span class="sxs-lookup"><span data-stu-id="29858-119">**GetStringArray method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getstringarray)
-   [<span data-ttu-id="29858-120">**Метод WebMethod**</span><span class="sxs-lookup"><span data-stu-id="29858-120">**GetTimeSpan method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-gettimespan)
-   [<span data-ttu-id="29858-121">**Метод ковариантности**</span><span class="sxs-lookup"><span data-stu-id="29858-121">**GetVariant method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getvariant)
-   [<span data-ttu-id="29858-122">**Метод GetWBEMINT16**</span><span class="sxs-lookup"><span data-stu-id="29858-122">**GetWBEMINT16 method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getwbemint16)
-   [<span data-ttu-id="29858-123">**Методы GetWBEMINT64**</span><span class="sxs-lookup"><span data-stu-id="29858-123">**GetWBEMINT64 methods**</span></span>](cinstance-getwbemint64.md)
-   [<span data-ttu-id="29858-124">**Метод GetWCHAR**</span><span class="sxs-lookup"><span data-stu-id="29858-124">**GetWCHAR method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getwchar)
-   [<span data-ttu-id="29858-125">**Метод "высловировать"**</span><span class="sxs-lookup"><span data-stu-id="29858-125">**GetWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getword)
-   [<span data-ttu-id="29858-126">**IsNull, метод**</span><span class="sxs-lookup"><span data-stu-id="29858-126">**IsNull method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-isnull)
-   [<span data-ttu-id="29858-127">**Метод сетбул**</span><span class="sxs-lookup"><span data-stu-id="29858-127">**Setbool method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setbool)
-   [<span data-ttu-id="29858-128">**Метод SetByte**</span><span class="sxs-lookup"><span data-stu-id="29858-128">**SetByte method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setbyte)
-   [<span data-ttu-id="29858-129">**Методы Сетчарсплат**</span><span class="sxs-lookup"><span data-stu-id="29858-129">**SetCharSplat methods**</span></span>](cinstance-setcharsplat.md)
-   [<span data-ttu-id="29858-130">**Методы Сетчстринг**</span><span class="sxs-lookup"><span data-stu-id="29858-130">**SetCHString methods**</span></span>](cinstance-setchstring.md)
-   [<span data-ttu-id="29858-131">**Метод Сетдатетиме**</span><span class="sxs-lookup"><span data-stu-id="29858-131">**SetDateTime method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setdatetime)
-   [<span data-ttu-id="29858-132">**Метод SetDOUBLE**</span><span class="sxs-lookup"><span data-stu-id="29858-132">**SetDOUBLE method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setdouble)
-   [<span data-ttu-id="29858-133">**Метод Сетдворд**</span><span class="sxs-lookup"><span data-stu-id="29858-133">**SetDWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setdword)
-   [<span data-ttu-id="29858-134">**Метод Сетембеддедобжект**</span><span class="sxs-lookup"><span data-stu-id="29858-134">**SetEmbeddedObject method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setembeddedobject)
-   [<span data-ttu-id="29858-135">**Метод SetNull**</span><span class="sxs-lookup"><span data-stu-id="29858-135">**SetNull method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setnull)
-   [<span data-ttu-id="29858-136">**Метод Сетстрингаррай**</span><span class="sxs-lookup"><span data-stu-id="29858-136">**SetStringArray method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setstringarray)
-   [<span data-ttu-id="29858-137">**Метод Сеттимеспан**</span><span class="sxs-lookup"><span data-stu-id="29858-137">**SetTimeSpan method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-settimespan)
-   [<span data-ttu-id="29858-138">**Метод Сетвариант**</span><span class="sxs-lookup"><span data-stu-id="29858-138">**SetVariant method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setvariant)
-   [<span data-ttu-id="29858-139">**Метод SetWBEMINT16**</span><span class="sxs-lookup"><span data-stu-id="29858-139">**SetWBEMINT16 method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setwbemint16)
-   [<span data-ttu-id="29858-140">**Метод Сетвчарсплат**</span><span class="sxs-lookup"><span data-stu-id="29858-140">**SetWCHARSplat method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setwcharsplat)
-   <span data-ttu-id="29858-141">[**Методы SetWBEMINT64**](/previous-versions/windows/desktop/legacy/aa389221(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="29858-141">[**SetWBEMINT64 methods**](/previous-versions/windows/desktop/legacy/aa389221(v=vs.85))</span></span>
-   [<span data-ttu-id="29858-142">**Метод Сетворд**</span><span class="sxs-lookup"><span data-stu-id="29858-142">**SetWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setword)

 

 
