---
description: В этом разделе описываются функции обработки строк оболочки Windows. Программные элементы, описанные в этой документации, экспортируются с помощью Shlwapi.dll и определяются в Shlwapi. h и Shlwapi. lib.
title: Функции обработки строк оболочки
ms.topic: article
ms.date: 05/31/2018
ms.assetid: c7329e22-c9bf-4845-bc0a-a155d1bd2005
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c2e47785db10ba7dc4bbe54e78e3a06be1b152a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999344"
---
# <a name="shell-string-handling-functions"></a><span data-ttu-id="eafec-104">Функции обработки строк оболочки</span><span class="sxs-lookup"><span data-stu-id="eafec-104">Shell String Handling Functions</span></span>

<span data-ttu-id="eafec-105">В этом разделе описываются функции обработки строк оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="eafec-105">This section describes the Windows Shell string handling functions.</span></span> <span data-ttu-id="eafec-106">Программные элементы, описанные в этой документации, экспортируются с помощью Shlwapi.dll и определяются в Shlwapi. h и Shlwapi. lib.</span><span class="sxs-lookup"><span data-stu-id="eafec-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="eafec-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="eafec-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eafec-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="eafec-108">Topic</span></span></th>
<th><span data-ttu-id="eafec-109">Описание</span><span class="sxs-lookup"><span data-stu-id="eafec-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eafec-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>чркмпи</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-111">Выполняет сравнение двух символов.</span><span class="sxs-lookup"><span data-stu-id="eafec-111">Performs a comparison between two characters.</span></span> <span data-ttu-id="eafec-112">Сравнение выполняется без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="eafec-112">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-113"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>жетакцептлангуажес</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-113"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-114">Извлекает строку, используемую с веб-сайтами при указании параметров языка.</span><span class="sxs-lookup"><span data-stu-id="eafec-114">Retrieves a string used with websites when specifying language preferences.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>интлстрекн</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-116">Выполняет сравнение указанного числа символов с начала двух локализованных строк с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="eafec-116">Performs a case-sensitive comparison of a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-117"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>интлстрекни</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-117"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-118">Выполняет сравнение указанного числа символов с начала двух локализованных строк без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="eafec-118">Performs a case-insensitive comparison of a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>интлстрекворкер</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-120">Сравнивает указанное число символов от начала двух локализованных строк.</span><span class="sxs-lookup"><span data-stu-id="eafec-120">Compares a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-121"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>исчарспаце</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-121"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-122">Определяет, представляет ли символ пробел.</span><span class="sxs-lookup"><span data-stu-id="eafec-122">Determines whether a character represents a space.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>шлоадиндиректстринг</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-124">Извлекает указанный текстовый ресурс, когда этот ресурс задается в виде непрямой строки (строка, которая начинается с символа "@").</span><span class="sxs-lookup"><span data-stu-id="eafec-124">Extracts a specified text resource when given that resource in the form of an indirect string (a string that begins with the '@' symbol).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>шстрдуп</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-126">Создает копию строки в только что выделенной памяти.</span><span class="sxs-lookup"><span data-stu-id="eafec-126">Makes a copy of a string in newly allocated memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-128">Добавляет одну строку в другую.</span><span class="sxs-lookup"><span data-stu-id="eafec-128">Appends one string to another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eafec-129">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="eafec-129">Do not use.</span></span> <span data-ttu-id="eafec-130">Дополнительные функции см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="eafec-130">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>стркатбуфф</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-132">Копирует символы из одной строки в другую, а затем добавляет их в конец.</span><span class="sxs-lookup"><span data-stu-id="eafec-132">Copies and appends characters from one string to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eafec-133">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="eafec-133">Do not use.</span></span> <span data-ttu-id="eafec-134">Дополнительные функции см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="eafec-134">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-135"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>стркатчаинв</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-135"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-136">Сцепляет две строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="eafec-136">Concatenates two Unicode strings.</span></span> <span data-ttu-id="eafec-137">Используется, если требуются повторные объединения в один и тот же буфер.</span><span class="sxs-lookup"><span data-stu-id="eafec-137">Used when repeated concatenations to the same buffer are required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-139">Ищет в строке первое вхождение символа, совпадающего с указанным символом.</span><span class="sxs-lookup"><span data-stu-id="eafec-139">Searches a string for the first occurrence of a character that matches the specified character.</span></span> <span data-ttu-id="eafec-140">При сравнении учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="eafec-140">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-141"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>стрчри</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-141"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-142">Ищет в строке первое вхождение символа, совпадающего с указанным символом.</span><span class="sxs-lookup"><span data-stu-id="eafec-142">Searches a string for the first occurrence of a character that matches the specified character.</span></span> <span data-ttu-id="eafec-143">Сравнение выполняется без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="eafec-143">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>стрчрнив</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-145">Ищет в строке первое вхождение указанного символа.</span><span class="sxs-lookup"><span data-stu-id="eafec-145">Searches a string for the first occurrence of a specified character.</span></span> <span data-ttu-id="eafec-146">Сравнение выполняется без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="eafec-146">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-147"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>стрчрнв</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-147"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-148">Ищет в строке первое вхождение указанного символа.</span><span class="sxs-lookup"><span data-stu-id="eafec-148">Searches a string for the first occurrence of a specified character.</span></span> <span data-ttu-id="eafec-149">При сравнении учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="eafec-149">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-151">Сравнивает две строки, чтобы определить, совпадают ли они.</span><span class="sxs-lookup"><span data-stu-id="eafec-151">Compares two strings to determine if they are the same.</span></span> <span data-ttu-id="eafec-152">При сравнении учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="eafec-152">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-153"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>стркмпк</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-153"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-154">Сравнивает строки с использованием правил сортировки времени выполнения языка C (ASCII).</span><span class="sxs-lookup"><span data-stu-id="eafec-154">Compares strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="eafec-155">При сравнении учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="eafec-155">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>стркмпи</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-157">Сравнивает две строки, чтобы определить, совпадают ли они.</span><span class="sxs-lookup"><span data-stu-id="eafec-157">Compares two strings to determine if they are the same.</span></span> <span data-ttu-id="eafec-158">Сравнение выполняется без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="eafec-158">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-159"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>стркмпик</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-159"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-160">Сравнивает две строки с помощью правил сортировки времени выполнения языка C (ASCII).</span><span class="sxs-lookup"><span data-stu-id="eafec-160">Compares two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="eafec-161">Сравнение выполняется без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="eafec-161">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-162"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>стркмплогикалв</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-162"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-163">Сравнивает две строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="eafec-163">Compares two Unicode strings.</span></span> <span data-ttu-id="eafec-164">Цифры в строках рассматриваются как числовое содержимое, а не как текст.</span><span class="sxs-lookup"><span data-stu-id="eafec-164">Digits in the strings are considered as numerical content rather than text.</span></span> <span data-ttu-id="eafec-165">В этом тесте регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="eafec-165">This test is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>стркмпн</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-167">Сравнивает указанное число символов от начала двух строк, чтобы определить, совпадают ли они.</span><span class="sxs-lookup"><span data-stu-id="eafec-167">Compares a specified number of characters from the beginning of two strings to determine if they are the same.</span></span> <span data-ttu-id="eafec-168">При сравнении учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="eafec-168">The comparison is case-sensitive.</span></span> <span data-ttu-id="eafec-169">Макрос <strong>StrNCmp</strong> отличается от этой функции только именем.</span><span class="sxs-lookup"><span data-stu-id="eafec-169">The <strong>StrNCmp</strong> macro differs from this function in name only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-170"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>стркмпнк</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-170"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-171">Сравнивает указанное число символов от начала двух строк с помощью правил сортировки времени выполнения языка C (ASCII).</span><span class="sxs-lookup"><span data-stu-id="eafec-171">Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="eafec-172">При сравнении учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="eafec-172">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-173"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>стркмпни</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-173"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-174">Сравнивает указанное число символов от начала двух строк, чтобы определить, совпадают ли они.</span><span class="sxs-lookup"><span data-stu-id="eafec-174">Compares a specified number of characters from the beginning of two strings to determine if they are the same.</span></span> <span data-ttu-id="eafec-175">Сравнение выполняется без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="eafec-175">The comparison is not case-sensitive.</span></span> <span data-ttu-id="eafec-176">Макрос <strong>стрнкмпи</strong> отличается от этой функции только именем.</span><span class="sxs-lookup"><span data-stu-id="eafec-176">The <strong>StrNCmpI</strong> macro differs from this function in name only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-177"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>стркмпник</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-177"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-178">Сравнивает указанное число символов от начала двух строк с помощью правил сортировки времени выполнения языка C (ASCII).</span><span class="sxs-lookup"><span data-stu-id="eafec-178">Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="eafec-179">Сравнение выполняется без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="eafec-179">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-180"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-180"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-181">Копирует одну строку в другую.</span><span class="sxs-lookup"><span data-stu-id="eafec-181">Copies one string to another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eafec-182">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="eafec-182">Do not use.</span></span> <span data-ttu-id="eafec-183">Дополнительные функции см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="eafec-183">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-184"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>стркпин</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-184"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpyN</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-185">Копирует указанное число символов с начала одной строки в другую.</span><span class="sxs-lookup"><span data-stu-id="eafec-185">Copies a specified number of characters from the beginning of one string to another.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eafec-186">Не используйте эту функцию или макрос <strong>StrNCpy</strong> .</span><span class="sxs-lookup"><span data-stu-id="eafec-186">Do not use this function or the <strong>StrNCpy</strong> macro.</span></span> <span data-ttu-id="eafec-187">Дополнительные функции см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="eafec-187">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-188"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>стркспн</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-188"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-189">Ищет в строке первое вхождение любой из групп символов.</span><span class="sxs-lookup"><span data-stu-id="eafec-189">Searches a string for the first occurrence of any of a group of characters.</span></span> <span data-ttu-id="eafec-190">В методе поиска учитывается регистр, а завершающий <strong>нуль</strong> -символ включается в соответствие шаблону поиска.</span><span class="sxs-lookup"><span data-stu-id="eafec-190">The search method is case-sensitive, and the terminating <strong>NULL</strong> character is included within the search pattern match.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-191"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>стркспни</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-191"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-192">Ищет в строке первое вхождение любой из групп символов.</span><span class="sxs-lookup"><span data-stu-id="eafec-192">Searches a string for the first occurrence of any of a group of characters.</span></span> <span data-ttu-id="eafec-193">В методе поиска регистр не учитывается, а завершающий <strong>нуль</strong> -символ включается в соответствие шаблону поиска.</span><span class="sxs-lookup"><span data-stu-id="eafec-193">The search method is not case-sensitive, and the terminating <strong>NULL</strong> character is included within the search pattern match.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-195">Дублирует строку.</span><span class="sxs-lookup"><span data-stu-id="eafec-195">Duplicates a string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-197">Преобразует числовое значение в строку, представляющую число, выраженное в байтах, килобайтах, мегабайтах или гигабайтах, в зависимости от размера.</span><span class="sxs-lookup"><span data-stu-id="eafec-197">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>стрформатбитесизеа</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-199">Преобразует числовое значение в строку, представляющую число, выраженное в байтах, килобайтах, мегабайтах или гигабайтах, в зависимости от размера.</span><span class="sxs-lookup"><span data-stu-id="eafec-199">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="eafec-200">Отличается от <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>стрформатбитесизев</strong></a> в одном типе параметра.</span><span class="sxs-lookup"><span data-stu-id="eafec-200">Differs from <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> in one parameter type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-201"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>стрформатбитесизикс</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-201"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-202">Преобразует числовое значение в строку, представляющую число в байтах, килобайтах, мегабайтах или гигабайтах в зависимости от размера.</span><span class="sxs-lookup"><span data-stu-id="eafec-202">Converts a numeric value into a string that represents the number in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="eafec-203">Расширяет <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>стрформатбитесизев</strong></a> , предлагая параметр для округления до ближайшей отображаемой цифры или для удаления неотображаемых цифр.</span><span class="sxs-lookup"><span data-stu-id="eafec-203">Extends <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> by offering the option to round to the nearest displayed digit or to discard undisplayed digits.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>стрформатбитесизев</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-205">Преобразует числовое значение в строку, представляющую число, выраженное в байтах, килобайтах, мегабайтах или гигабайтах, в зависимости от размера.</span><span class="sxs-lookup"><span data-stu-id="eafec-205">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="eafec-206">Отличается от <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>стрформатбитесизеа</strong></a> в одном типе параметра.</span><span class="sxs-lookup"><span data-stu-id="eafec-206">Differs from <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> in one parameter type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-207"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>стрформаткбсизе</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-207"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-208">Преобразует числовое значение в строку, представляющую число, выраженное в виде значения размера в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="eafec-208">Converts a numeric value into a string that represents the number expressed as a size value in kilobytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-209"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>стрфромтимеинтервал</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-209"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-210">Преобразует интервал времени, указанный в миллисекундах, в строку.</span><span class="sxs-lookup"><span data-stu-id="eafec-210">Converts a time interval, specified in milliseconds, to a string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>стрисинтлекуал</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-212">Сравнивает указанное число символов от начала двух строк, чтобы определить, равны ли они.</span><span class="sxs-lookup"><span data-stu-id="eafec-212">Compares a specified number of characters from the beginning of two strings to determine if they are equal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-214">Добавляет указанное число символов от начала одной строки к концу другой.</span><span class="sxs-lookup"><span data-stu-id="eafec-214">Appends a specified number of characters from the beginning of one string to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eafec-215">Не используйте эту функцию или макрос <strong>стркатн</strong> .</span><span class="sxs-lookup"><span data-stu-id="eafec-215">Do not use this function or the <strong>StrCatN</strong> macro.</span></span> <span data-ttu-id="eafec-216">Дополнительные функции см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="eafec-216">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-217"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>стрпбрк</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-217"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-218">Ищет в строке первое вхождение символа, содержащегося в указанном буфере.</span><span class="sxs-lookup"><span data-stu-id="eafec-218">Searches a string for the first occurrence of a character contained in a specified buffer.</span></span> <span data-ttu-id="eafec-219">Этот поиск не включает завершающий нуль символ.</span><span class="sxs-lookup"><span data-stu-id="eafec-219">This search does not include the terminating null character.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-220"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-220"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-221">Выполняет поиск в строке последнего вхождения указанного символа.</span><span class="sxs-lookup"><span data-stu-id="eafec-221">Searches a string for the last occurrence of a specified character.</span></span> <span data-ttu-id="eafec-222">При сравнении учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="eafec-222">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-223"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>стррчри</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-223"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-224">Выполняет поиск в строке последнего вхождения указанного символа.</span><span class="sxs-lookup"><span data-stu-id="eafec-224">Searches a string for the last occurrence of a specified character.</span></span> <span data-ttu-id="eafec-225">Сравнение выполняется без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="eafec-225">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-226"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>стрреттобстр</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-226"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-227">Принимает структуру <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>стррет</strong></a> , возвращенную <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>Ишеллфолдер:: жетдисплайнамеоф</strong></a> , которая содержит или указывает на строку, и возвращает эту строку в виде <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="eafec-227">Accepts a <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> that contains or points to a string, and returns that string as a <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-228"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>стрреттобуф</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-228"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-229">Преобразует структуру <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>стррет</strong></a> , возвращенную <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>Ишеллфолдер:: жетдисплайнамеоф</strong></a> , в строку и помещает результат в буфер.</span><span class="sxs-lookup"><span data-stu-id="eafec-229">Converts an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> to a string, and places the result in a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-230"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>стрреттостр</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-230"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-231">Принимает структуру <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>стррет</strong></a> , возвращенную <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>Ишеллфолдер:: жетдисплайнамеоф</strong></a> , и возвращает указатель на выделенную строку, содержащую отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="eafec-231">Takes an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> and returns a pointer to an allocated string containing the display name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-232"><a href="strrettostrn.md"><strong>стрреттострн</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-232"><a href="strrettostrn.md"><strong>StrRetToStrN</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-233">Принимает структуру <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>стррет</strong></a> , возвращенную <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>Ишеллфолдер:: жетдисплайнамеоф</strong></a>, преобразует ее в строку и помещает результат в буфер.</span><span class="sxs-lookup"><span data-stu-id="eafec-233">Takes an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a>, converts it to a string, and places the result in a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>стррстри</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-235">Выполняет поиск последнего вхождения указанной подстроки в строку.</span><span class="sxs-lookup"><span data-stu-id="eafec-235">Searches for the last occurrence of a specified substring within a string.</span></span> <span data-ttu-id="eafec-236">Сравнение выполняется без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="eafec-236">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-237"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-237"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-238">Получает длину подстроки в строке, которая состоит исключительно из символов, содержащихся в указанном буфере.</span><span class="sxs-lookup"><span data-stu-id="eafec-238">Obtains the length of a substring within a string that consists entirely of characters contained in a specified buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-239"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>стрстр</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-239"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-240">Находит первое вхождение подстроки в строке.</span><span class="sxs-lookup"><span data-stu-id="eafec-240">Finds the first occurrence of a substring within a string.</span></span> <span data-ttu-id="eafec-241">При сравнении учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="eafec-241">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>стрстри</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-243">Находит первое вхождение подстроки в строке.</span><span class="sxs-lookup"><span data-stu-id="eafec-243">Finds the first occurrence of a substring within a string.</span></span> <span data-ttu-id="eafec-244">Сравнение выполняется без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="eafec-244">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-245"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>стртоинт</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-245"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-246">Преобразует строку, представляющую десятичное значение, в целое число.</span><span class="sxs-lookup"><span data-stu-id="eafec-246">Converts a string that represents a decimal value to an integer.</span></span> <span data-ttu-id="eafec-247">Макрос <strong>стртолонг</strong> идентичен этой функции.</span><span class="sxs-lookup"><span data-stu-id="eafec-247">The <strong>StrToLong</strong> macro is identical to this function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-249">Преобразует строку, представляющую десятичное или шестнадцатеричное значение, в 64-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="eafec-249">Converts a string representing a decimal or hexadecimal value to a 64-bit integer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>стртоинтекс</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-251">Преобразует строку, представляющую десятичное или шестнадцатеричное число, в целое число.</span><span class="sxs-lookup"><span data-stu-id="eafec-251">Converts a string representing a decimal or hexadecimal number to an integer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-252"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>стртрим</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-252"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>StrTrim</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-253">Удаляет указанные начальные и конечные символы из строки.</span><span class="sxs-lookup"><span data-stu-id="eafec-253">Removes specified leading and trailing characters from a string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafec-254"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>внспринтф</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-254"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-255">Принимает список аргументов переменной длины и возвращает значения аргументов как отформатированную строку в стиле <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="eafec-255">Takes a variable-length argument list and returns the values of the arguments as a <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>-style formatted string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eafec-256">Не используйте эту функцию.</span><span class="sxs-lookup"><span data-stu-id="eafec-256">Do not use this function.</span></span> <span data-ttu-id="eafec-257">Дополнительные функции см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="eafec-257">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafec-258"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>ввнспринтф</strong></a></span><span class="sxs-lookup"><span data-stu-id="eafec-258"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a></span></span><br/></td>
<td><span data-ttu-id="eafec-259">Принимает список аргументов и возвращает значения аргументов как отформатированную строку в стиле <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="eafec-259">Takes a list of arguments and returns the values of the arguments as a <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>-style formatted string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eafec-260">Не используйте эту функцию.</span><span class="sxs-lookup"><span data-stu-id="eafec-260">Do not use this function.</span></span> <span data-ttu-id="eafec-261">Дополнительные функции см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="eafec-261">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
