---
description: В этом разделе определяются идентификаторы календаря (тип данных КАЛИД), используемые для указания различных календарей.
ms.assetid: ba2e841e-e24e-476a-851e-a29b3af4f04d
title: Идентификаторы календаря
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9b931aea4a186af0849dfe8f6642c53744d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809515"
---
# <a name="calendar-identifiers"></a><span data-ttu-id="e3827-103">Идентификаторы календаря</span><span class="sxs-lookup"><span data-stu-id="e3827-103">Calendar Identifiers</span></span>

<span data-ttu-id="e3827-104">В этом разделе определяются идентификаторы календаря (тип данных КАЛИД), используемые для указания различных календарей.</span><span class="sxs-lookup"><span data-stu-id="e3827-104">This topic defines the calendar identifiers (data type CALID) that are used to specify different calendars.</span></span> <span data-ttu-id="e3827-105">Приложения могут использовать эти идентификаторы при использовании следующих функций многоязыковой поддержки и функций обратного вызова, которые имеют параметры, принимающие тип данных КАЛИД:</span><span class="sxs-lookup"><span data-stu-id="e3827-105">Your applications can use these identifiers when using the following NLS functions and callback functions, which have parameters that take the CALID data type:</span></span>

-   [<span data-ttu-id="e3827-106">**конвертсистемтиметокалдатетиме**</span><span class="sxs-lookup"><span data-stu-id="e3827-106">**ConvertSystemTimeToCalDateTime**</span></span>](convertsystemtimetocaldatetime.md)
-   [<span data-ttu-id="e3827-107">**енумкалендаринфо**</span><span class="sxs-lookup"><span data-stu-id="e3827-107">**EnumCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa)
-   [<span data-ttu-id="e3827-108">**енумкалендаринфоекс**</span><span class="sxs-lookup"><span data-stu-id="e3827-108">**EnumCalendarInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)
-   [<span data-ttu-id="e3827-109">**енумкалендаринфоексекс**</span><span class="sxs-lookup"><span data-stu-id="e3827-109">**EnumCalendarInfoExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)
-   <span data-ttu-id="e3827-110">[**енумкалендаринфопроцекс**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e3827-110">[**EnumCalendarInfoProcEx**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))</span></span>
-   <span data-ttu-id="e3827-111">[**енумдатеформатспроцекс**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e3827-111">[**EnumDateFormatsProcEx**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))</span></span>
-   [<span data-ttu-id="e3827-112">**жеткалендаринфо**</span><span class="sxs-lookup"><span data-stu-id="e3827-112">**GetCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)
-   [<span data-ttu-id="e3827-113">**жеткалендаринфоекс**</span><span class="sxs-lookup"><span data-stu-id="e3827-113">**GetCalendarInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)
-   [<span data-ttu-id="e3827-114">**жеткалендарсуппортеддатеранже**</span><span class="sxs-lookup"><span data-stu-id="e3827-114">**GetCalendarSupportedDateRange**</span></span>](getcalendarsupporteddaterange.md)
-   [<span data-ttu-id="e3827-115">**искалендарлеапеар**</span><span class="sxs-lookup"><span data-stu-id="e3827-115">**IsCalendarLeapYear**</span></span>](iscalendarleapyear.md)
-   [<span data-ttu-id="e3827-116">**сеткалендаринфо**</span><span class="sxs-lookup"><span data-stu-id="e3827-116">**SetCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa)

<span data-ttu-id="e3827-117">Определены следующие значения.</span><span class="sxs-lookup"><span data-stu-id="e3827-117">The following values are defined.</span></span> <span data-ttu-id="e3827-118">Все остальные значения зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="e3827-118">All other values are reserved.</span></span> <span data-ttu-id="e3827-119">Эти значения нельзя сочетать друг с другом.</span><span class="sxs-lookup"><span data-stu-id="e3827-119">These values cannot be combined with one another.</span></span>



<span data-ttu-id="e3827-120">Идентификатор календаря</span><span class="sxs-lookup"><span data-stu-id="e3827-120">Calendar identifier</span></span>

<span data-ttu-id="e3827-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e3827-121">Meaning</span></span>

<span data-ttu-id="e3827-122">1</span><span class="sxs-lookup"><span data-stu-id="e3827-122">1</span></span>

<span data-ttu-id="e3827-123">CAL, \_ григорианский</span><span class="sxs-lookup"><span data-stu-id="e3827-123">CAL\_GREGORIAN</span></span>

<span data-ttu-id="e3827-124">Григорианский (локализованный)</span><span class="sxs-lookup"><span data-stu-id="e3827-124">Gregorian (localized)</span></span>

<span data-ttu-id="e3827-125">2</span><span class="sxs-lookup"><span data-stu-id="e3827-125">2</span></span>

<span data-ttu-id="e3827-126">CAL \_ григорианского \_ США</span><span class="sxs-lookup"><span data-stu-id="e3827-126">CAL\_GREGORIAN\_US</span></span>

<span data-ttu-id="e3827-127">Григорианский (строки на английском языке всегда)</span><span class="sxs-lookup"><span data-stu-id="e3827-127">Gregorian (English strings always)</span></span>

<span data-ttu-id="e3827-128">3</span><span class="sxs-lookup"><span data-stu-id="e3827-128">3</span></span>

<span data-ttu-id="e3827-129">Клиентская лицензия для \_ Японии</span><span class="sxs-lookup"><span data-stu-id="e3827-129">CAL\_JAPAN</span></span>

<span data-ttu-id="e3827-130">Японская эра императора</span><span class="sxs-lookup"><span data-stu-id="e3827-130">Japanese Emperor Era</span></span>

<span data-ttu-id="e3827-131">4</span><span class="sxs-lookup"><span data-stu-id="e3827-131">4</span></span>

<span data-ttu-id="e3827-132">CAL, \_ Тайвань</span><span class="sxs-lookup"><span data-stu-id="e3827-132">CAL\_TAIWAN</span></span>

<span data-ttu-id="e3827-133">Тайваньский календарь</span><span class="sxs-lookup"><span data-stu-id="e3827-133">Taiwan calendar</span></span>

<span data-ttu-id="e3827-134">5</span><span class="sxs-lookup"><span data-stu-id="e3827-134">5</span></span>

<span data-ttu-id="e3827-135">\_Корея CAL</span><span class="sxs-lookup"><span data-stu-id="e3827-135">CAL\_KOREA</span></span>

<span data-ttu-id="e3827-136">Тангуная эра корейского языка</span><span class="sxs-lookup"><span data-stu-id="e3827-136">Korean Tangun Era</span></span>

<span data-ttu-id="e3827-137">6</span><span class="sxs-lookup"><span data-stu-id="e3827-137">6</span></span>

<span data-ttu-id="e3827-138">CAL \_ Хиджра</span><span class="sxs-lookup"><span data-stu-id="e3827-138">CAL\_HIJRI</span></span>

<span data-ttu-id="e3827-139">Хиджра (арабский лунный)</span><span class="sxs-lookup"><span data-stu-id="e3827-139">Hijri (Arabic Lunar)</span></span>

<span data-ttu-id="e3827-140">7</span><span class="sxs-lookup"><span data-stu-id="e3827-140">7</span></span>

<span data-ttu-id="e3827-141">\_тайская лицензия</span><span class="sxs-lookup"><span data-stu-id="e3827-141">CAL\_THAI</span></span>

<span data-ttu-id="e3827-142">Тайский</span><span class="sxs-lookup"><span data-stu-id="e3827-142">Thai</span></span>

<span data-ttu-id="e3827-143">8</span><span class="sxs-lookup"><span data-stu-id="e3827-143">8</span></span>

<span data-ttu-id="e3827-144">CAL для \_ иврита</span><span class="sxs-lookup"><span data-stu-id="e3827-144">CAL\_HEBREW</span></span>

<span data-ttu-id="e3827-145">Иврит (лунный)</span><span class="sxs-lookup"><span data-stu-id="e3827-145">Hebrew (Lunar)</span></span>

<span data-ttu-id="e3827-146">9</span><span class="sxs-lookup"><span data-stu-id="e3827-146">9</span></span>

<span data-ttu-id="e3827-147">CAL, \_ григорианский, \_ \_ французский</span><span class="sxs-lookup"><span data-stu-id="e3827-147">CAL\_GREGORIAN\_ME\_FRENCH</span></span>

<span data-ttu-id="e3827-148">Gregorian Middle East French</span><span class="sxs-lookup"><span data-stu-id="e3827-148">Gregorian Middle East French</span></span>

<span data-ttu-id="e3827-149">10</span><span class="sxs-lookup"><span data-stu-id="e3827-149">10</span></span>

<span data-ttu-id="e3827-150">CAL \_ григорианский \_ Арабский</span><span class="sxs-lookup"><span data-stu-id="e3827-150">CAL\_GREGORIAN\_ARABIC</span></span>

<span data-ttu-id="e3827-151">Gregorian Arabic</span><span class="sxs-lookup"><span data-stu-id="e3827-151">Gregorian Arabic</span></span>

<span data-ttu-id="e3827-152">11</span><span class="sxs-lookup"><span data-stu-id="e3827-152">11</span></span>

<span data-ttu-id="e3827-153">CAL \_ григорианский \_ кслит ( \_ Английский)</span><span class="sxs-lookup"><span data-stu-id="e3827-153">CAL\_GREGORIAN\_XLIT\_ENGLISH</span></span>

<span data-ttu-id="e3827-154">Григорианский транслитерированный (английский)</span><span class="sxs-lookup"><span data-stu-id="e3827-154">Gregorian transliterated English</span></span>

<span data-ttu-id="e3827-155">12</span><span class="sxs-lookup"><span data-stu-id="e3827-155">12</span></span>

<span data-ttu-id="e3827-156">CAL \_ григорианского \_ кслит \_ французский</span><span class="sxs-lookup"><span data-stu-id="e3827-156">CAL\_GREGORIAN\_XLIT\_FRENCH</span></span>

<span data-ttu-id="e3827-157">Григорианский транслитерированный французский</span><span class="sxs-lookup"><span data-stu-id="e3827-157">Gregorian transliterated French</span></span>

<span data-ttu-id="e3827-158">23</span><span class="sxs-lookup"><span data-stu-id="e3827-158">23</span></span>

<span data-ttu-id="e3827-159">CAL \_ умалкура</span><span class="sxs-lookup"><span data-stu-id="e3827-159">CAL\_UMALQURA</span></span>

<span data-ttu-id="e3827-160">**Windows Vista и более поздние версии:** Календарь аль-Кура (арабский лунный)</span><span class="sxs-lookup"><span data-stu-id="e3827-160">**Windows Vista and later:** Um Al Qura (Arabic lunar) calendar</span></span>



 

> [!Note]  
> <span data-ttu-id="e3827-161">Пропускная нумерация между идентификаторами CAL \_ григорианский \_ кслит \_ французский и Cal \_ умалкура является преднамеренной.</span><span class="sxs-lookup"><span data-stu-id="e3827-161">The gap in numbering between the identifiers CAL\_GREGORIAN\_XLIT\_FRENCH and CAL\_UMALQURA is intentional.</span></span> <span data-ttu-id="e3827-162">Обозначение CAL \_ умалкура — 23, а не 13.</span><span class="sxs-lookup"><span data-stu-id="e3827-162">The designator for CAL\_UMALQURA is 23, not 13.</span></span>

 

<span data-ttu-id="e3827-163">Кроме того, [**енумкалендаринфо**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) и [**енумкалендаринфоекс**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) позволяют использовать значение перечислить \_ все \_ календари для запроса перечисления всех применимых календарей.</span><span class="sxs-lookup"><span data-stu-id="e3827-163">In addition, [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) and [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) allow the use of the value ENUM\_ALL\_CALENDARS to request an enumeration of all applicable calendars.</span></span>

<span data-ttu-id="e3827-164">Значение</span><span class="sxs-lookup"><span data-stu-id="e3827-164">Value</span></span>

<span data-ttu-id="e3827-165">Значение</span><span class="sxs-lookup"><span data-stu-id="e3827-165">Meaning</span></span>

<span data-ttu-id="e3827-166">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="e3827-166">0xffffffff</span></span>

<span data-ttu-id="e3827-167">перечислить \_ все \_ календари</span><span class="sxs-lookup"><span data-stu-id="e3827-167">ENUM\_ALL\_CALENDARS</span></span>

<span data-ttu-id="e3827-168">Все применимые календари для указанного языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="e3827-168">All applicable calendars for the specified locale</span></span>



 

 

 
