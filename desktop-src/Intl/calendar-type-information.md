---
description: В этом разделе описывается информация о типе календаря (тип данных КАЛТИПЕ), используемая в функциях Енумкалендаринфо, Енумкалендаринфоекс, Енумкалендаринфоексекс, Жеткалендаринфо и GetCalendarInfoEx.
ms.assetid: 33361a97-0f27-477a-a0ee-3d4d3aaeaacf
title: Сведения о типе календаря
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a8e334a1b05f372f51c81ab8158294d46eebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912564"
---
# <a name="calendar-type-information"></a><span data-ttu-id="af0b3-103">Сведения о типе календаря</span><span class="sxs-lookup"><span data-stu-id="af0b3-103">Calendar Type Information</span></span>

<span data-ttu-id="af0b3-104">В этом разделе описывается информация о типе календаря (тип данных КАЛТИПЕ), используемая в функциях [**енумкалендаринфо**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**енумкалендаринфоекс**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**енумкалендаринфоексекс**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**жеткалендаринфо**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)и [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) .</span><span class="sxs-lookup"><span data-stu-id="af0b3-104">This topic describes the calendar type information (CALTYPE data type) used in the [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa), and [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) functions.</span></span> <span data-ttu-id="af0b3-105">Некоторые из этих значений также используются функцией [**сеткалендаринфо**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) .</span><span class="sxs-lookup"><span data-stu-id="af0b3-105">Some of these values are also used by the [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) function.</span></span>

<span data-ttu-id="af0b3-106">Следующие константы КАЛТИПЕ можно использовать в сочетании с любыми другими константами КАЛТИПЕ.</span><span class="sxs-lookup"><span data-stu-id="af0b3-106">The following CALTYPE constants can be used in combination with any other CALTYPE constants.</span></span>



| <span data-ttu-id="af0b3-107">Константа</span><span class="sxs-lookup"><span data-stu-id="af0b3-107">Constant</span></span>                     | <span data-ttu-id="af0b3-108">Описание</span><span class="sxs-lookup"><span data-stu-id="af0b3-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af0b3-109">CAL \_ наусероверриде</span><span class="sxs-lookup"><span data-stu-id="af0b3-109">CAL\_NOUSEROVERRIDE</span></span>          | <span data-ttu-id="af0b3-110">**Windows Me/98, windows 2000:** Используйте систему по умолчанию вместо выбора пользователя.</span><span class="sxs-lookup"><span data-stu-id="af0b3-110">**Windows Me/98, Windows 2000:** Use the system default instead of the user's choice.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="af0b3-111">клиентские лицензии \_ возвращают \_ \_ имена женитиве</span><span class="sxs-lookup"><span data-stu-id="af0b3-111">CAL\_RETURN\_GENITIVE\_NAMES</span></span> | <span data-ttu-id="af0b3-112">**Windows 7 и более поздние версии:** Получение результата из [**жеткалендаринфо**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) в виде женитиве названий месяцев, которые являются именами, используемыми при объединении названий месяцев с другими элементами.</span><span class="sxs-lookup"><span data-stu-id="af0b3-112">**Windows 7 and later:** Retrieve the result from [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) in the form of genitive names of months, which are the names used when the month names are combined with other items.</span></span> <span data-ttu-id="af0b3-113">Например, в украинский эквивалент в январе записывается как «січень», когда месяц называется «только один».</span><span class="sxs-lookup"><span data-stu-id="af0b3-113">For example, in Ukrainian the equivalent of January is written "Січень" when the month is named alone.</span></span> <span data-ttu-id="af0b3-114">Однако если название месяца используется в сочетании, например, в дате, например 5 января 2003, используется женитиве форма имени.</span><span class="sxs-lookup"><span data-stu-id="af0b3-114">However, when the month name is used in combination, for example, in a date such as January 5th, 2003, the genitive form of the name is used.</span></span> <span data-ttu-id="af0b3-115">Для примера "Украинский" название месяца женитиве отображается как "5 січня 2003".</span><span class="sxs-lookup"><span data-stu-id="af0b3-115">For the Ukrainian example, the genitive month name is displayed as "5 січня 2003".</span></span> <span data-ttu-id="af0b3-116">Дополнительные сведения см. в [статье \_ return \_ женитиве \_ names](locale-return-constants.md).</span><span class="sxs-lookup"><span data-stu-id="af0b3-116">For more information, see [LOCALE\_RETURN\_GENITIVE\_NAMES](locale-return-constants.md).</span></span> |
| <span data-ttu-id="af0b3-117">\_номер возврата \_ CAL</span><span class="sxs-lookup"><span data-stu-id="af0b3-117">CAL\_RETURN\_NUMBER</span></span>          | <span data-ttu-id="af0b3-118">**Windows Me/98, windows 2000:** Получение результата из [**жеткалендаринфо**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) в виде числа, а не строки.</span><span class="sxs-lookup"><span data-stu-id="af0b3-118">**Windows Me/98, Windows 2000:** Retrieve the result from [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) as a number instead of a string.</span></span> <span data-ttu-id="af0b3-119">Это допустимо только для значений, начинающихся с лицензии CAL \_ I.</span><span class="sxs-lookup"><span data-stu-id="af0b3-119">This is only valid for values beginning with CAL\_I.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="af0b3-120">CAL \_ использование \_ CP \_ ACP</span><span class="sxs-lookup"><span data-stu-id="af0b3-120">CAL\_USE\_CP\_ACP</span></span>            | <span data-ttu-id="af0b3-121">**Windows Me/98, windows 2000:** Используйте системную кодовую страницу ANSI (ACP) вместо кодовой страницы языкового стандарта для перевода строк.</span><span class="sxs-lookup"><span data-stu-id="af0b3-121">**Windows Me/98, Windows 2000:** Use the system ANSI code page (ACP) instead of the locale code page for string translation.</span></span> <span data-ttu-id="af0b3-122">Это относится только к версиям функций ANSI, например **енумкалендаринфоа**.</span><span class="sxs-lookup"><span data-stu-id="af0b3-122">This is only relevant for ANSI versions of functions, for example, **EnumCalendarInfoA**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="af0b3-123">Следующие константы КАЛТИПЕ являются взаимоисключающими и не могут использоваться в сочетании друг с другом в вызове функции.</span><span class="sxs-lookup"><span data-stu-id="af0b3-123">The following CALTYPE constants are mutually exclusive and cannot be used in combination with each other in a function call.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af0b3-124">Константа</span><span class="sxs-lookup"><span data-stu-id="af0b3-124">Constant</span></span></th>
<th><span data-ttu-id="af0b3-125">Описание</span><span class="sxs-lookup"><span data-stu-id="af0b3-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="af0b3-126">CAL_ICALINTVALUE</span><span class="sxs-lookup"><span data-stu-id="af0b3-126">CAL_ICALINTVALUE</span></span></td>
<td><span data-ttu-id="af0b3-127">Целочисленное значение, указывающее тип календаря для альтернативного календаря.</span><span class="sxs-lookup"><span data-stu-id="af0b3-127">An integer value indicating the calendar type of the alternate calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-128">CAL_ITWODIGITYEARMAX</span><span class="sxs-lookup"><span data-stu-id="af0b3-128">CAL_ITWODIGITYEARMAX</span></span></td>
<td><span data-ttu-id="af0b3-129"><strong>Windows Me/98, windows 2000:</strong> Целочисленное значение, указывающее верхнюю границу диапазона из двух цифр года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-129"><strong>Windows Me/98, Windows 2000:</strong> An integer value indicating the upper boundary of the two-digit year range.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-130">CAL_IYEAROFFSETRANGE</span><span class="sxs-lookup"><span data-stu-id="af0b3-130">CAL_IYEAROFFSETRANGE</span></span></td>
<td><span data-ttu-id="af0b3-131">Одна или несколько строк, заканчивающихся нулем, которые задают смещения года для каждого диапазона эры.</span><span class="sxs-lookup"><span data-stu-id="af0b3-131">One or more null-terminated strings that specify the year offsets for each of the era ranges.</span></span> <span data-ttu-id="af0b3-132">Последняя строка содержит дополнительный завершающий нуль символ.</span><span class="sxs-lookup"><span data-stu-id="af0b3-132">The last string has an extra terminating null character.</span></span> <span data-ttu-id="af0b3-133">Это значение зависит от типа необязательного календаря.</span><span class="sxs-lookup"><span data-stu-id="af0b3-133">This value varies in format depending on the type of optional calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-134">CAL_SABBREVDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="af0b3-134">CAL_SABBREVDAYNAME1</span></span></td>
<td><span data-ttu-id="af0b3-135">Сокращенное собственное имя первого дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-135">Abbreviated native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-136">CAL_SABBREVDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="af0b3-136">CAL_SABBREVDAYNAME2</span></span></td>
<td><span data-ttu-id="af0b3-137">Сокращенное собственное имя второго дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-137">Abbreviated native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-138">CAL_SABBREVDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="af0b3-138">CAL_SABBREVDAYNAME3</span></span></td>
<td><span data-ttu-id="af0b3-139">Сокращенное собственное название третьего дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-139">Abbreviated native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-140">CAL_SABBREVDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="af0b3-140">CAL_SABBREVDAYNAME4</span></span></td>
<td><span data-ttu-id="af0b3-141">Сокращенное собственное имя четвертого дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-141">Abbreviated native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-142">CAL_SABBREVDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="af0b3-142">CAL_SABBREVDAYNAME5</span></span></td>
<td><span data-ttu-id="af0b3-143">Сокращенное машинное имя пятого дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-143">Abbreviated native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-144">CAL_SABBREVDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="af0b3-144">CAL_SABBREVDAYNAME6</span></span></td>
<td><span data-ttu-id="af0b3-145">Сокращенное собственное название шестого дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-145">Abbreviated native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-146">CAL_SABBREVDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="af0b3-146">CAL_SABBREVDAYNAME7</span></span></td>
<td><span data-ttu-id="af0b3-147">Сокращенное собственное имя седьмого дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-147">Abbreviated native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-148">CAL_SABBREVERASTRING</span><span class="sxs-lookup"><span data-stu-id="af0b3-148">CAL_SABBREVERASTRING</span></span></td>
<td><span data-ttu-id="af0b3-149"><strong>Windows 7 и более поздние версии:</strong> Сокращенное машинное имя эры.</span><span class="sxs-lookup"><span data-stu-id="af0b3-149"><strong>Windows 7 and later:</strong> Abbreviated native name of an era.</span></span> <span data-ttu-id="af0b3-150">Полная эра представляется константой CAL_SERASTRING.</span><span class="sxs-lookup"><span data-stu-id="af0b3-150">The full era is represented by the CAL_SERASTRING constant.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-151">CAL_SABBREVMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="af0b3-151">CAL_SABBREVMONTHNAME1</span></span></td>
<td><span data-ttu-id="af0b3-152">Сокращенное собственное имя первого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-152">Abbreviated native name of the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-153">CAL_SABBREVMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="af0b3-153">CAL_SABBREVMONTHNAME2</span></span></td>
<td><span data-ttu-id="af0b3-154">Сокращенное собственное имя второго месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-154">Abbreviated native name of the second month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-155">CAL_SABBREVMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="af0b3-155">CAL_SABBREVMONTHNAME3</span></span></td>
<td><span data-ttu-id="af0b3-156">Сокращенное собственное название третьего месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-156">Abbreviated native name of the third month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-157">CAL_SABBREVMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="af0b3-157">CAL_SABBREVMONTHNAME4</span></span></td>
<td><span data-ttu-id="af0b3-158">Сокращенное собственное название четвертого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-158">Abbreviated native name of the fourth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-159">CAL_SABBREVMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="af0b3-159">CAL_SABBREVMONTHNAME5</span></span></td>
<td><span data-ttu-id="af0b3-160">Сокращенное машинное имя пятого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-160">Abbreviated native name of the fifth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-161">CAL_SABBREVMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="af0b3-161">CAL_SABBREVMONTHNAME6</span></span></td>
<td><span data-ttu-id="af0b3-162">Сокращенное собственное название шестого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-162">Abbreviated native name of the sixth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-163">CAL_SABBREVMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="af0b3-163">CAL_SABBREVMONTHNAME7</span></span></td>
<td><span data-ttu-id="af0b3-164">Сокращенное собственное имя седьмого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-164">Abbreviated native name of the seventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-165">CAL_SABBREVMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="af0b3-165">CAL_SABBREVMONTHNAME8</span></span></td>
<td><span data-ttu-id="af0b3-166">Сокращенное собственное название восьмого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-166">Abbreviated native name of the eighth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-167">CAL_SABBREVMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="af0b3-167">CAL_SABBREVMONTHNAME9</span></span></td>
<td><span data-ttu-id="af0b3-168">Сокращенное машинное имя девятого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-168">Abbreviated native name of the ninth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-169">CAL_SABBREVMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="af0b3-169">CAL_SABBREVMONTHNAME10</span></span></td>
<td><span data-ttu-id="af0b3-170">Сокращенное собственное название десятого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-170">Abbreviated native name of the tenth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-171">CAL_SABBREVMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="af0b3-171">CAL_SABBREVMONTHNAME11</span></span></td>
<td><span data-ttu-id="af0b3-172">Сокращенное имя в машинном номере одиннадцатого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-172">Abbreviated native name of the eleventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-173">CAL_SABBREVMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="af0b3-173">CAL_SABBREVMONTHNAME12</span></span></td>
<td><span data-ttu-id="af0b3-174">Сокращенное собственное название двенадцатого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-174">Abbreviated native name of the twelfth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-175">CAL_SABBREVMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="af0b3-175">CAL_SABBREVMONTHNAME13</span></span></td>
<td><span data-ttu-id="af0b3-176">Сокращенное машинное имя тринадцатого месяца года, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="af0b3-176">Abbreviated native name of the thirteenth month of the year, if it exists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-177">CAL_SCALNAME</span><span class="sxs-lookup"><span data-stu-id="af0b3-177">CAL_SCALNAME</span></span></td>
<td><span data-ttu-id="af0b3-178">Собственное имя альтернативного календаря.</span><span class="sxs-lookup"><span data-stu-id="af0b3-178">Native name of the alternate calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-179">CAL_SDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="af0b3-179">CAL_SDAYNAME1</span></span></td>
<td><span data-ttu-id="af0b3-180">Собственное имя первого дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-180">Native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-181">CAL_SDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="af0b3-181">CAL_SDAYNAME2</span></span></td>
<td><span data-ttu-id="af0b3-182">Собственное имя второго дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-182">Native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-183">CAL_SDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="af0b3-183">CAL_SDAYNAME3</span></span></td>
<td><span data-ttu-id="af0b3-184">Собственное название третьего дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-184">Native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-185">CAL_SDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="af0b3-185">CAL_SDAYNAME4</span></span></td>
<td><span data-ttu-id="af0b3-186">Собственное название четвертого дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-186">Native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-187">CAL_SDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="af0b3-187">CAL_SDAYNAME5</span></span></td>
<td><span data-ttu-id="af0b3-188">Собственное имя пятого дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-188">Native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-189">CAL_SDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="af0b3-189">CAL_SDAYNAME6</span></span></td>
<td><span data-ttu-id="af0b3-190">Собственное название шестого дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-190">Native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-191">CAL_SDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="af0b3-191">CAL_SDAYNAME7</span></span></td>
<td><span data-ttu-id="af0b3-192">Собственное название седьмого дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-192">Native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-193">CAL_SERASTRING</span><span class="sxs-lookup"><span data-stu-id="af0b3-193">CAL_SERASTRING</span></span></td>
<td><span data-ttu-id="af0b3-194">Одна или несколько строк, заканчивающихся нулем, которые задают каждую из кодовых позиций Юникода, указывающих эру, связанную с CAL_IYEAROFFSETRANGE.</span><span class="sxs-lookup"><span data-stu-id="af0b3-194">One or more null-terminated strings that specify each of the Unicode code points specifying the era associated with CAL_IYEAROFFSETRANGE.</span></span> <span data-ttu-id="af0b3-195">Последняя строка содержит дополнительный завершающий нуль символ.</span><span class="sxs-lookup"><span data-stu-id="af0b3-195">The last string has an extra terminating null character.</span></span> <span data-ttu-id="af0b3-196">Это значение зависит от типа необязательного календаря.</span><span class="sxs-lookup"><span data-stu-id="af0b3-196">This value varies in format depending on the type of optional calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-197">CAL_SLONGDATE</span><span class="sxs-lookup"><span data-stu-id="af0b3-197">CAL_SLONGDATE</span></span></td>
<td><span data-ttu-id="af0b3-198">Длинные форматы даты для типа календаря.</span><span class="sxs-lookup"><span data-stu-id="af0b3-198">Long date formats for the calendar type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-199">CAL_SMONTHDAY</span><span class="sxs-lookup"><span data-stu-id="af0b3-199">CAL_SMONTHDAY</span></span></td>
<td><span data-ttu-id="af0b3-200"><strong>Windows 7 и более поздние версии:</strong> Формат месяца и дня для типа календаря.</span><span class="sxs-lookup"><span data-stu-id="af0b3-200"><strong>Windows 7 and later:</strong> Format of the month and day for the calendar type.</span></span> <span data-ttu-id="af0b3-201">Форматирование аналогично форматированию для CAL_SLONGDATE.</span><span class="sxs-lookup"><span data-stu-id="af0b3-201">The formatting is similar to that for CAL_SLONGDATE.</span></span> <span data-ttu-id="af0b3-202">Например, если шаблон "месяц/день" представляет собой полное название месяца, за которым следует номер дня с начальными нулями, например, &quot; 03 сентября, &quot; то используется формат &quot; мммм дд &quot; .</span><span class="sxs-lookup"><span data-stu-id="af0b3-202">For example, if the Month/Day pattern is the full month name followed by the day number with leading zeros, for example, &quot;September 03&quot;, the format is &quot;MMMM dd&quot;.</span></span> <span data-ttu-id="af0b3-203">Одинарные кавычки можно использовать для вставки неформатированных символов, например de в испанском.</span><span class="sxs-lookup"><span data-stu-id="af0b3-203">Single quotation marks can be used to insert non-format characters, for example, 'de' in Spanish.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="af0b3-204">Этот тип календаря поддерживает только один формат.</span><span class="sxs-lookup"><span data-stu-id="af0b3-204">This calendar type supports only one format.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-205">CAL_SMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="af0b3-205">CAL_SMONTHNAME1</span></span></td>
<td><span data-ttu-id="af0b3-206">Собственное имя первого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-206">Native name of the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-207">CAL_SMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="af0b3-207">CAL_SMONTHNAME2</span></span></td>
<td><span data-ttu-id="af0b3-208">Собственное имя второго месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-208">Native name of the second month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-209">CAL_SMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="af0b3-209">CAL_SMONTHNAME3</span></span></td>
<td><span data-ttu-id="af0b3-210">Собственное название третьего месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-210">Native name of the third month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-211">CAL_SMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="af0b3-211">CAL_SMONTHNAME4</span></span></td>
<td><span data-ttu-id="af0b3-212">Собственное название четвертого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-212">Native name of the fourth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-213">CAL_SMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="af0b3-213">CAL_SMONTHNAME5</span></span></td>
<td><span data-ttu-id="af0b3-214">Собственное название пятого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-214">Native name of the fifth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-215">CAL_SMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="af0b3-215">CAL_SMONTHNAME6</span></span></td>
<td><span data-ttu-id="af0b3-216">Собственное название шестого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-216">Native name of the sixth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-217">CAL_SMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="af0b3-217">CAL_SMONTHNAME7</span></span></td>
<td><span data-ttu-id="af0b3-218">Собственное название седьмого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-218">Native name of the seventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-219">CAL_SMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="af0b3-219">CAL_SMONTHNAME8</span></span></td>
<td><span data-ttu-id="af0b3-220">Собственное название восьмого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-220">Native name of the eighth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-221">CAL_SMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="af0b3-221">CAL_SMONTHNAME9</span></span></td>
<td><span data-ttu-id="af0b3-222">Собственное название девятого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-222">Native name of the ninth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-223">CAL_SMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="af0b3-223">CAL_SMONTHNAME10</span></span></td>
<td><span data-ttu-id="af0b3-224">Собственное название десятого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-224">Native name of the tenth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-225">CAL_SMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="af0b3-225">CAL_SMONTHNAME11</span></span></td>
<td><span data-ttu-id="af0b3-226">Собственное название одиннадцатого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-226">Native name of the eleventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-227">CAL_SMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="af0b3-227">CAL_SMONTHNAME12</span></span></td>
<td><span data-ttu-id="af0b3-228">Собственное название двенадцатого месяца года.</span><span class="sxs-lookup"><span data-stu-id="af0b3-228">Native name of the twelfth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-229">CAL_SMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="af0b3-229">CAL_SMONTHNAME13</span></span></td>
<td><span data-ttu-id="af0b3-230">Собственное имя тринадцатого месяца года, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="af0b3-230">Native name of the thirteenth month of the year, if it exists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-231">CAL_SSHORTDATE</span><span class="sxs-lookup"><span data-stu-id="af0b3-231">CAL_SSHORTDATE</span></span></td>
<td><span data-ttu-id="af0b3-232">Краткие форматы даты для типа календаря.</span><span class="sxs-lookup"><span data-stu-id="af0b3-232">Short date formats for the calendar type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-233">CAL_SSHORTESTDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="af0b3-233">CAL_SSHORTESTDAYNAME1</span></span></td>
<td><span data-ttu-id="af0b3-234"><strong>Windows Vista и более поздние версии:</strong> Короткое собственное имя первого дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-234"><strong>Windows Vista and later:</strong> Short native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-235">CAL_SSHORTESTDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="af0b3-235">CAL_SSHORTESTDAYNAME2</span></span></td>
<td><span data-ttu-id="af0b3-236"><strong>Windows Vista и более поздние версии:</strong> Короткое собственное имя второго дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-236"><strong>Windows Vista and later:</strong> Short native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-237">CAL_SSHORTESTDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="af0b3-237">CAL_SSHORTESTDAYNAME3</span></span></td>
<td><span data-ttu-id="af0b3-238"><strong>Windows Vista и более поздние версии:</strong> Короткое машинное имя третьего дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-238"><strong>Windows Vista and later:</strong> Short native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-239">CAL_SSHORTESTDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="af0b3-239">CAL_SSHORTESTDAYNAME4</span></span></td>
<td><span data-ttu-id="af0b3-240"><strong>Windows Vista и более поздние версии:</strong> Короткое собственное имя четвертого дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-240"><strong>Windows Vista and later:</strong> Short native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-241">CAL_SSHORTESTDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="af0b3-241">CAL_SSHORTESTDAYNAME5</span></span></td>
<td><span data-ttu-id="af0b3-242"><strong>Windows Vista и более поздние версии:</strong> Короткое машинное имя пятого дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-242"><strong>Windows Vista and later:</strong> Short native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-243">CAL_SSHORTESTDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="af0b3-243">CAL_SSHORTESTDAYNAME6</span></span></td>
<td><span data-ttu-id="af0b3-244"><strong>Windows Vista и более поздние версии:</strong> Короткое машинное имя шестого дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-244"><strong>Windows Vista and later:</strong> Short native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af0b3-245">CAL_SSHORTESTDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="af0b3-245">CAL_SSHORTESTDAYNAME7</span></span></td>
<td><span data-ttu-id="af0b3-246"><strong>Windows Vista и более поздние версии:</strong> Короткое машинное имя седьмого дня недели.</span><span class="sxs-lookup"><span data-stu-id="af0b3-246"><strong>Windows Vista and later:</strong> Short native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af0b3-247">CAL_SYEARMONTH</span><span class="sxs-lookup"><span data-stu-id="af0b3-247">CAL_SYEARMONTH</span></span></td>
<td><span data-ttu-id="af0b3-248"><strong>Windows Me/98, windows 2000:</strong> Форматы "год/месяц" для указанных календарей.</span><span class="sxs-lookup"><span data-stu-id="af0b3-248"><strong>Windows Me/98, Windows 2000:</strong> The year/month formats for the specified calendars.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="af0b3-249">Если собственное имя дня недели или месяца является пустой строкой, это имя идентично имени, указанному в соответствующей информации о языковых стандартах, и, следовательно, не дублируется здесь.</span><span class="sxs-lookup"><span data-stu-id="af0b3-249">If the native name for the day of the week or for a month is an empty string, that name is identical to the name specified in the corresponding locale information and therefore is not duplicated here.</span></span>

 

 

 




