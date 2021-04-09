---
description: Класс Чстринг предоставляет следующие методы.
ms.assetid: C064D6DE-14C4-4143-8164-B367C10CBF8E
ms.tgt_platform: multiple
title: Методы Чстринг
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e15a26bf2b5945990f8cd37ee67c2953395ca98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081004"
---
# <a name="chstring-methods"></a><span data-ttu-id="fcaf2-103">Методы Чстринг</span><span class="sxs-lookup"><span data-stu-id="fcaf2-103">CHString Methods</span></span>

<span data-ttu-id="fcaf2-104">\[Класс [**чстринг**](chstring.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="fcaf2-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="fcaf2-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="fcaf2-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="fcaf2-106">Класс [**чстринг**](chstring.md) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="fcaf2-106">The [**CHString**](chstring.md) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fcaf2-107">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="fcaf2-107">In this section</span></span>

-   [<span data-ttu-id="fcaf2-108">**Метод Аллоксисстринг**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-108">**AllocSysString method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)
-   <span data-ttu-id="fcaf2-109">[**Конструкторы Чстринг**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-109">[**CHString constructors**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))</span></span>
-   [<span data-ttu-id="fcaf2-110">**Метод COLLATE**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-110">**Collate method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-collate)
-   [<span data-ttu-id="fcaf2-111">**Compare - метод**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-111">**Compare method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-compare)
-   [<span data-ttu-id="fcaf2-112">**Метод Компаренокасе**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-112">**CompareNoCase method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)
-   [<span data-ttu-id="fcaf2-113">**Пустой метод**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-113">**Empty method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-empty)
-   <span data-ttu-id="fcaf2-114">[**Поиск методов**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-114">[**Find methods**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))</span></span>
-   [<span data-ttu-id="fcaf2-115">**Метод Финдонеоф**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-115">**FindOneOf method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)
-   <span data-ttu-id="fcaf2-116">[**Методы форматирования**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-116">[**Format methods**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))</span></span>
-   <span data-ttu-id="fcaf2-117">[**Методы Форматмессажев**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-117">[**FormatMessageW methods**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))</span></span>
-   [<span data-ttu-id="fcaf2-118">**Метод Форматв**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-118">**FormatV method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)
-   [<span data-ttu-id="fcaf2-119">**Метод Фриекстра**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-119">**FreeExtra method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)
-   [<span data-ttu-id="fcaf2-120">**Метод Жеталлокленгс**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-120">**GetAllocLength method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)
-   <span data-ttu-id="fcaf2-121">[**Метод GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-121">[**GetAt method**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))</span></span>
-   [<span data-ttu-id="fcaf2-122">**GetBuffer - метод**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-122">**GetBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)
-   [<span data-ttu-id="fcaf2-123">**Метод Жетбуфферсетленгс**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-123">**GetBufferSetLength method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength)
-   [<span data-ttu-id="fcaf2-124">**Метод GetData**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-124">**GetData method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)
-   [<span data-ttu-id="fcaf2-125">**Метод DATALENGTH**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-125">**GetLength method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)
-   [<span data-ttu-id="fcaf2-126">**IsEmpty - метод**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-126">**IsEmpty method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)
-   [<span data-ttu-id="fcaf2-127">**Метод Left**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-127">**Left method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-left)
-   <span data-ttu-id="fcaf2-128">[**Метод Лоадстрингв**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-128">[**LoadStringW method**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))</span></span>
-   [<span data-ttu-id="fcaf2-129">**Метод Локкбуффер**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-129">**LockBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)
-   [<span data-ttu-id="fcaf2-130">**Метод Макеловер**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-130">**MakeLower method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)
-   [<span data-ttu-id="fcaf2-131">**Метод Макереверсе**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-131">**MakeReverse method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)
-   [<span data-ttu-id="fcaf2-132">**Метод Макеуппер**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-132">**MakeUpper method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)
-   <span data-ttu-id="fcaf2-133">[**Методы mid**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-133">[**Mid methods**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span></span>
-   <span data-ttu-id="fcaf2-134">[**\[ \] метод оператора**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-134">[**operator\[\] method**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))</span></span>
-   [<span data-ttu-id="fcaf2-135">**Чстринг:: operator +**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-135">**CHString::operator+**</span></span>](chstring--operator-plus.md)
-   [<span data-ttu-id="fcaf2-136">**Чстринг:: operator + =**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-136">**CHString::operator+=**</span></span>](chstring--operator-plus-equal.md)
-   [<span data-ttu-id="fcaf2-137">**Чстринг:: operator =**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-137">**CHString::operator=**</span></span>](chstring--operator-equal.md)
-   <span data-ttu-id="fcaf2-138">[**operator = = (Констчстринг&, Констчстринг&) метод**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-138">[**operator==(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))</span></span>
-   <span data-ttu-id="fcaf2-139">[**operator = = (Констчстринг&, Констлпквстр&) метод**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-139">[**operator==(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))</span></span>
-   <span data-ttu-id="fcaf2-140">[**метод> оператора (Констчстринг&, Констчстринг&)**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-140">[**operator>(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))</span></span>
-   <span data-ttu-id="fcaf2-141">[**метод> оператора (Констчстринг&, Констлпквстр&)**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-141">[**operator>(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))</span></span>
-   <span data-ttu-id="fcaf2-142">[**operator>= (Констчстринг&, Констчстринг&) метод**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-142">[**operator>=(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))</span></span>
-   <span data-ttu-id="fcaf2-143">[**operator>= (Констчстринг&, Констлпквстр&) метод**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-143">[**operator>=(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))</span></span>
-   <span data-ttu-id="fcaf2-144">[**метод< оператора (Констчстринг&, Констчстринг&)**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-144">[**operator<(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))</span></span>
-   <span data-ttu-id="fcaf2-145">[**метод< оператора (Констчстринг&, Констлпквстр&)**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-145">[**operator<(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))</span></span>
-   <span data-ttu-id="fcaf2-146">[**operator<= (Констчстринг&, Констчстринг&) метод**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-146">[**operator<=(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))</span></span>
-   <span data-ttu-id="fcaf2-147">[**operator<= (Констчстринг&, Констлпквстр&) метод**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-147">[**operator<=(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))</span></span>
-   <span data-ttu-id="fcaf2-148">[**operator! = (Констчстринг&, Констчстринг&) метод**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-148">[**operator!=(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))</span></span>
-   <span data-ttu-id="fcaf2-149">[**operator! = (Констчстринг&, Констлпквстр&) метод**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcaf2-149">[**operator!=(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))</span></span>
-   [<span data-ttu-id="fcaf2-150">**operator ЛПКВСТР, метод**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-150">**operator LPCWSTR method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)
-   [<span data-ttu-id="fcaf2-151">**Метод Релеасебуффер**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-151">**ReleaseBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)
-   [<span data-ttu-id="fcaf2-152">**Метод Реверсефинд**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-152">**ReverseFind method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)
-   [<span data-ttu-id="fcaf2-153">**Метод right**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-153">**Right method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-right)
-   [<span data-ttu-id="fcaf2-154">**Метод SetAt**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-154">**SetAt method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-setat)
-   [<span data-ttu-id="fcaf2-155">**Метод Спанексклудинг**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-155">**SpanExcluding method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)
-   [<span data-ttu-id="fcaf2-156">**Метод Спанинклудинг**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-156">**SpanIncluding method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)
-   [<span data-ttu-id="fcaf2-157">**Метод Тримлефт**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-157">**TrimLeft method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)
-   [<span data-ttu-id="fcaf2-158">**Метод Тримригхт**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-158">**TrimRight method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)
-   [<span data-ttu-id="fcaf2-159">**Метод Унлоккбуффер**</span><span class="sxs-lookup"><span data-stu-id="fcaf2-159">**UnlockBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)

 

 
