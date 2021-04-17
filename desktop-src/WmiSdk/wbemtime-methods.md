---
description: Класс Вбемтиме предоставляет следующие методы.
ms.assetid: 56B21156-8FD2-4FF8-805E-DDA63C897F80
ms.tgt_platform: multiple
title: Методы WBEMTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e77c338f3d1d0657e20bfe6b819c9976d00d45f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693684"
---
# <a name="wbemtime-methods"></a><span data-ttu-id="325f0-103">Методы WBEMTime</span><span class="sxs-lookup"><span data-stu-id="325f0-103">WBEMTime Methods</span></span>

<span data-ttu-id="325f0-104">\[Класс [**вбемтиме**](wbemtime.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="325f0-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="325f0-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="325f0-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="325f0-106">Класс [**вбемтиме**](wbemtime.md) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="325f0-106">The [**WBEMTime**](wbemtime.md) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="325f0-107">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="325f0-107">In this section</span></span>

-   [<span data-ttu-id="325f0-108">**Метод Clear**</span><span class="sxs-lookup"><span data-stu-id="325f0-108">**Clear method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-clear)
-   [<span data-ttu-id="325f0-109">**GetBSTR - метод**</span><span class="sxs-lookup"><span data-stu-id="325f0-109">**GetBSTR method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getbstr)
-   [<span data-ttu-id="325f0-110">**Метод Жетдмтф**</span><span class="sxs-lookup"><span data-stu-id="325f0-110">**GetDMTF method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtf)
-   [<span data-ttu-id="325f0-111">**Метод Жетдмтфноннтфс**</span><span class="sxs-lookup"><span data-stu-id="325f0-111">**GetDMTFNonNtfs method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtfnonntfs)
-   [<span data-ttu-id="325f0-112">**Метод функции getFileTime**</span><span class="sxs-lookup"><span data-stu-id="325f0-112">**GetFILETIME method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getfiletime)
-   <span data-ttu-id="325f0-113">[**Методы Жетлокалоффсетфордате**](/previous-versions/windows/desktop/legacy/aa394049(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="325f0-113">[**GetLocalOffsetForDate methods**](/previous-versions/windows/desktop/legacy/aa394049(v=vs.85))</span></span>
-   [<span data-ttu-id="325f0-114">**Метод Жетструкттм**</span><span class="sxs-lookup"><span data-stu-id="325f0-114">**GetStructtm method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getstructtm)
-   [<span data-ttu-id="325f0-115">**Метод GetSYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="325f0-115">**GetSYSTEMTIME method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getsystemtime)
-   [<span data-ttu-id="325f0-116">**Метод метода Time**</span><span class="sxs-lookup"><span data-stu-id="325f0-116">**GetTime method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime)
-   [<span data-ttu-id="325f0-117">**\_Метод t**</span><span class="sxs-lookup"><span data-stu-id="325f0-117">**Gettime\_t method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime_t)
-   [<span data-ttu-id="325f0-118">**Метод исок**</span><span class="sxs-lookup"><span data-stu-id="325f0-118">**IsOk method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-isok)
-   <span data-ttu-id="325f0-119">[**операторы operator**](/previous-versions/windows/desktop/legacy/aa394051(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="325f0-119">[**operator- operators**](/previous-versions/windows/desktop/legacy/aa394051(v=vs.85))</span></span>
-   [<span data-ttu-id="325f0-120">**Метод Вбемтиме:: operator! =**</span><span class="sxs-lookup"><span data-stu-id="325f0-120">**WBEMTime::operator != method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-not-equal-to)
-   [<span data-ttu-id="325f0-121">**Метод < Вбемтиме:: operator**</span><span class="sxs-lookup"><span data-stu-id="325f0-121">**WBEMTime::operator < method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than)
-   [<span data-ttu-id="325f0-122">**Вбемтиме:: operator <= метод**</span><span class="sxs-lookup"><span data-stu-id="325f0-122">**WBEMTime::operator <= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than-equal-to)
-   [<span data-ttu-id="325f0-123">**Метод Вбемтиме:: operator = =**</span><span class="sxs-lookup"><span data-stu-id="325f0-123">**WBEMTime::operator == method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-equal-equal-to)
-   [<span data-ttu-id="325f0-124">**Метод > Вбемтиме:: operator**</span><span class="sxs-lookup"><span data-stu-id="325f0-124">**WBEMTime::operator > method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)
-   [<span data-ttu-id="325f0-125">**Вбемтиме:: operator >= метод**</span><span class="sxs-lookup"><span data-stu-id="325f0-125">**WBEMTime::operator >= method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)
-   [<span data-ttu-id="325f0-126">**operator +, метод**</span><span class="sxs-lookup"><span data-stu-id="325f0-126">**operator+ method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-add)
-   [<span data-ttu-id="325f0-127">**operator + =, метод**</span><span class="sxs-lookup"><span data-stu-id="325f0-127">**operator+= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-add-assign)
-   <span data-ttu-id="325f0-128">[**operator = операторы**](/previous-versions/windows/desktop/legacy/aa394050(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="325f0-128">[**operator= operators**](/previous-versions/windows/desktop/legacy/aa394050(v=vs.85))</span></span>
-   [<span data-ttu-id="325f0-129">**operator-= метод**</span><span class="sxs-lookup"><span data-stu-id="325f0-129">**operator-= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-sub-assign)
-   [<span data-ttu-id="325f0-130">**Метод Сетдмтф**</span><span class="sxs-lookup"><span data-stu-id="325f0-130">**SetDMTF method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-setdmtf)
-   <span data-ttu-id="325f0-131">[**Конструкторы Вбемтиме**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span><span class="sxs-lookup"><span data-stu-id="325f0-131">[**WBEMTime constructors**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span></span>

 

 
