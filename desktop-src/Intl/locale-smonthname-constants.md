---
description: '\_Константы смонснаме языкового стандарта \*'
ms.assetid: 81269282-bea8-4a5d-929d-c68af34bd1ac
title: Константы LOCALE_SMONTHNAME *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4b45a84ea31d7d8c3d5de6e2f3f3a452c7a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810751"
---
# <a name="locale_smonthname-constants"></a><span data-ttu-id="57c8c-103">\_Константы смонснаме языкового стандарта \*</span><span class="sxs-lookup"><span data-stu-id="57c8c-103">LOCALE\_SMONTHNAME\* Constants</span></span>

<span data-ttu-id="57c8c-104">В этом разделе определяются \_ константы СМОНСНАМЕ локали \* , используемые NLS.</span><span class="sxs-lookup"><span data-stu-id="57c8c-104">This topic defines the LOCALE\_SMONTHNAME\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="57c8c-105">Значение</span><span class="sxs-lookup"><span data-stu-id="57c8c-105">Value</span></span></th>
<th><span data-ttu-id="57c8c-106">Значение</span><span class="sxs-lookup"><span data-stu-id="57c8c-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="57c8c-107">LOCALE_SMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="57c8c-107">LOCALE_SMONTHNAME1</span></span></td>
<td><span data-ttu-id="57c8c-108">Собственное длинное имя в январе.</span><span class="sxs-lookup"><span data-stu-id="57c8c-108">Native long name for January.</span></span> <span data-ttu-id="57c8c-109">Максимально допустимое число символов для этой строки — 80, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="57c8c-109">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="57c8c-110">Вызов функции <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> или <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> с константой LOCALE_SMONTHNAME \* возвращает отдельную или сопоставленную форму названия месяца.</span><span class="sxs-lookup"><span data-stu-id="57c8c-110">Calling the <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> or <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> function with a LOCALE_SMONTHNAME\* constant returns the standalone, or nominative, form of the month name.</span></span> <span data-ttu-id="57c8c-111">Чтобы получить форму женитиве названия месяца, приложение вызывает <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata">жетдатеформат</a> или <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">Жетдатеформатекс</a> с датой ддмммм и удаляет две цифры из начала полученной строки.</span><span class="sxs-lookup"><span data-stu-id="57c8c-111">To get the genitive form of the month name, the application calls <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata">GetDateFormat</a> or <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a> with a date picture of ddMMMM and removes the two digits from the beginning of the retrieved string.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57c8c-112">LOCALE_SMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="57c8c-112">LOCALE_SMONTHNAME2</span></span></td>
<td><span data-ttu-id="57c8c-113">Собственное полное имя в феврале.</span><span class="sxs-lookup"><span data-stu-id="57c8c-113">Native long name for February.</span></span> <span data-ttu-id="57c8c-114">Максимально допустимое число символов для этой строки — 80, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="57c8c-114">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="57c8c-115">См. Примечание для LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="57c8c-115">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57c8c-116">LOCALE_SMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="57c8c-116">LOCALE_SMONTHNAME3</span></span></td>
<td><span data-ttu-id="57c8c-117">Собственное длинное имя в марте.</span><span class="sxs-lookup"><span data-stu-id="57c8c-117">Native long name for March.</span></span> <span data-ttu-id="57c8c-118">Максимально допустимое число символов для этой строки — 80, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="57c8c-118">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="57c8c-119">См. Примечание для LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="57c8c-119">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57c8c-120">LOCALE_SMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="57c8c-120">LOCALE_SMONTHNAME4</span></span></td>
<td><span data-ttu-id="57c8c-121">Собственное длинное имя в апреле.</span><span class="sxs-lookup"><span data-stu-id="57c8c-121">Native long name for April.</span></span> <span data-ttu-id="57c8c-122">Максимально допустимое число символов для этой строки — 80, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="57c8c-122">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="57c8c-123">См. Примечание для LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="57c8c-123">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57c8c-124">LOCALE_SMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="57c8c-124">LOCALE_SMONTHNAME5</span></span></td>
<td><span data-ttu-id="57c8c-125">Собственное длинное имя для Май.</span><span class="sxs-lookup"><span data-stu-id="57c8c-125">Native long name for May.</span></span> <span data-ttu-id="57c8c-126">Максимально допустимое число символов для этой строки — 80, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="57c8c-126">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="57c8c-127">См. Примечание для LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="57c8c-127">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57c8c-128">LOCALE_SMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="57c8c-128">LOCALE_SMONTHNAME6</span></span></td>
<td><span data-ttu-id="57c8c-129">Собственное длинное имя в июне.</span><span class="sxs-lookup"><span data-stu-id="57c8c-129">Native long name for June.</span></span> <span data-ttu-id="57c8c-130">Максимально допустимое число символов для этой строки — 80, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="57c8c-130">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="57c8c-131">См. Примечание для LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="57c8c-131">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57c8c-132">LOCALE_SMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="57c8c-132">LOCALE_SMONTHNAME7</span></span></td>
<td><span data-ttu-id="57c8c-133">Собственное длинное имя в июле.</span><span class="sxs-lookup"><span data-stu-id="57c8c-133">Native long name for July.</span></span> <span data-ttu-id="57c8c-134">Максимально допустимое число символов для этой строки — 80, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="57c8c-134">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="57c8c-135">См. Примечание для LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="57c8c-135">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57c8c-136">LOCALE_SMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="57c8c-136">LOCALE_SMONTHNAME8</span></span></td>
<td><span data-ttu-id="57c8c-137">Собственное длинное имя в августе.</span><span class="sxs-lookup"><span data-stu-id="57c8c-137">Native long name for August.</span></span> <span data-ttu-id="57c8c-138">Максимально допустимое число символов для этой строки — 80, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="57c8c-138">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="57c8c-139">См. Примечание для LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="57c8c-139">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57c8c-140">LOCALE_SMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="57c8c-140">LOCALE_SMONTHNAME9</span></span></td>
<td><span data-ttu-id="57c8c-141">Собственное длинное имя в сентябре.</span><span class="sxs-lookup"><span data-stu-id="57c8c-141">Native long name for September.</span></span> <span data-ttu-id="57c8c-142">Максимально допустимое число символов для этой строки — 80, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="57c8c-142">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="57c8c-143">См. Примечание для LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="57c8c-143">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57c8c-144">LOCALE_SMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="57c8c-144">LOCALE_SMONTHNAME10</span></span></td>
<td><span data-ttu-id="57c8c-145">Собственное длинное имя в октябре.</span><span class="sxs-lookup"><span data-stu-id="57c8c-145">Native long name for October.</span></span> <span data-ttu-id="57c8c-146">Максимально допустимое число символов для этой строки — 80, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="57c8c-146">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="57c8c-147">См. Примечание для LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="57c8c-147">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57c8c-148">LOCALE_SMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="57c8c-148">LOCALE_SMONTHNAME11</span></span></td>
<td><span data-ttu-id="57c8c-149">Собственное длинное имя в ноябре.</span><span class="sxs-lookup"><span data-stu-id="57c8c-149">Native long name for November.</span></span> <span data-ttu-id="57c8c-150">Максимально допустимое число символов для этой строки — 80, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="57c8c-150">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="57c8c-151">См. Примечание для LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="57c8c-151">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57c8c-152">LOCALE_SMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="57c8c-152">LOCALE_SMONTHNAME12</span></span></td>
<td><span data-ttu-id="57c8c-153">Собственное длинное имя в декабре.</span><span class="sxs-lookup"><span data-stu-id="57c8c-153">Native long name for December.</span></span> <span data-ttu-id="57c8c-154">Максимально допустимое число символов для этой строки — 80, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="57c8c-154">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="57c8c-155">См. Примечание для LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="57c8c-155">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57c8c-156">LOCALE_SMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="57c8c-156">LOCALE_SMONTHNAME13</span></span></td>
<td><span data-ttu-id="57c8c-157">Собственное имя за 13-й месяц, если он существует.</span><span class="sxs-lookup"><span data-stu-id="57c8c-157">Native name for a 13th month, if it exists.</span></span> <span data-ttu-id="57c8c-158">Максимально допустимое число символов для этой строки — 80, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="57c8c-158">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="57c8c-159">См. Примечание для LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="57c8c-159">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




