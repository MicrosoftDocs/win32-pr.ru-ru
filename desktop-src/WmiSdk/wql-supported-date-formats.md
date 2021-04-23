---
description: Описывает форматы даты, поддерживаемые для использования в предложении языка WQL.
ms.assetid: 24d70b7f-681b-4a36-bb67-beaf69f4919f
ms.tgt_platform: multiple
title: WQL-Supported форматы даты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01e5741de24943defc4df0e59e7255bc1a37effd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910271"
---
# <a name="wql-supported-date-formats"></a><span data-ttu-id="3ad5d-103">WQL-Supported форматы даты</span><span class="sxs-lookup"><span data-stu-id="3ad5d-103">WQL-Supported Date Formats</span></span>

<span data-ttu-id="3ad5d-104">Помимо формата **DateTime** WMI, для использования в предложении **WHERE** WQL поддерживаются следующие форматы даты.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-104">In addition to the WMI **DATETIME** format, the following date formats are supported for use in the WQL **WHERE** clause.</span></span>

<span data-ttu-id="3ad5d-105">Формат отображения времени различается для разных языков.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-105">The displayed time format is different for different locales.</span></span> <span data-ttu-id="3ad5d-106">Сценарии, подключающиеся к удаленным компьютерам, должны указывать время в формате, соответствующем языковому стандарту конечного компьютера.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-106">Scripts that connect to remote computers must specify time in the format appropriate for the locale of the target computer.</span></span>

<span data-ttu-id="3ad5d-107">Например, США формат даты и времени — MM-ДД-ГГГГ.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-107">For example, the United States date and time format is MM-DD-YYYY.</span></span> <span data-ttu-id="3ad5d-108">Если сценарий на компьютере с США подключается к целевому компьютеру в формате дд-мм-гггг, запросы обрабатываются на целевом компьютере как дд-мм-гггг.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-108">If a script on a US computer connects to a target computer in a locale where the format is DD-MM-YYYY, then queries are processed on the target computer as DD-MM-YYYY.</span></span> <span data-ttu-id="3ad5d-109">Чтобы избежать различных результатов между языками, используйте формат [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="3ad5d-109">To avoid different results between locales, use the [**DATETIME**](datetime.md) format.</span></span> <span data-ttu-id="3ad5d-110">Дополнительные сведения см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="3ad5d-110">For more information, see [Date and Time Format](date-and-time-format.md).</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3ad5d-111">Формат</span><span class="sxs-lookup"><span data-stu-id="3ad5d-111">Format</span></span></th>
<th><span data-ttu-id="3ad5d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="3ad5d-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ad5d-113">Пн [TH] дд [,] [гг] гг</span><span class="sxs-lookup"><span data-stu-id="3ad5d-113">Mon[th] dd[,] [yy]yy</span></span></td>
<td><span data-ttu-id="3ad5d-114">Месяц (написанный или сокращенный), день, необязательная запятая и два или четыре цифры года.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-114">Month (either spelled-out or abbreviated in three letters), day, optional comma, and two or four-digit year.</span></span><br/> <dl> <span data-ttu-id="3ad5d-115">21 января 1932 г.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-115">January 21, 1932</span></span><br />
<span data-ttu-id="3ad5d-116">21 января 32 г.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-116">January 21, 32</span></span><br />
<span data-ttu-id="3ad5d-117">Янв 21 1932</span><span class="sxs-lookup"><span data-stu-id="3ad5d-117">Jan 21 1932</span></span><br />
<span data-ttu-id="3ad5d-118">Янв 21 32</span><span class="sxs-lookup"><span data-stu-id="3ad5d-118">Jan 21 32</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ad5d-119">Мес [TH] [,] гггг</span><span class="sxs-lookup"><span data-stu-id="3ad5d-119">Mon[th][,] yyyy</span></span></td>
<td><span data-ttu-id="3ad5d-120">Месяц (написанный или сокращенный), необязательная запятая и 4-значный год.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-120">Month (either spelled-out or abbreviated in three letters), optional comma, and four-digit year.</span></span><br/> <dl> <span data-ttu-id="3ad5d-121">1932 января</span><span class="sxs-lookup"><span data-stu-id="3ad5d-121">January 1932</span></span><br />
<span data-ttu-id="3ad5d-122">Янв 1932</span><span class="sxs-lookup"><span data-stu-id="3ad5d-122">Jan 1932</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ad5d-123">Мес [TH] [гг] гг дд</span><span class="sxs-lookup"><span data-stu-id="3ad5d-123">Mon[th] [yy]yy dd</span></span></td>
<td><span data-ttu-id="3ad5d-124">Месяц (написанный или сокращенный), два или четыре цифры, год и день.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-124">Month (either spelled-out or abbreviated in three letters), two or four digit year, and day.</span></span><br/> <dl> <span data-ttu-id="3ad5d-125">1932 21 января</span><span class="sxs-lookup"><span data-stu-id="3ad5d-125">January 1932 21</span></span><br />
<span data-ttu-id="3ad5d-126">Янв 32 21</span><span class="sxs-lookup"><span data-stu-id="3ad5d-126">Jan 32 21</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ad5d-127">DD мес [TH] [,] [] [гг] гг</span><span class="sxs-lookup"><span data-stu-id="3ad5d-127">dd Mon[th][,][ ][yy]yy</span></span></td>
<td><span data-ttu-id="3ad5d-128">День месяца, месяца (написанный или сокращенный), необязательная запятая, дополнительное пространство и два или четыре цифры года.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-128">Day of the month, month (either spelled-out or abbreviated in three letters), optional comma, optional space, and two or four-digit year.</span></span><br/> <dl> <span data-ttu-id="3ad5d-129">21 января, 1932</span><span class="sxs-lookup"><span data-stu-id="3ad5d-129">21 January, 1932</span></span><br />
<span data-ttu-id="3ad5d-130">21 Jan32</span><span class="sxs-lookup"><span data-stu-id="3ad5d-130">21 Jan32</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ad5d-131">дд [гг] гг мес [TH]</span><span class="sxs-lookup"><span data-stu-id="3ad5d-131">dd [yy]yy Mon[th]</span></span></td>
<td><span data-ttu-id="3ad5d-132">День месяца, два или четыре цифры года и месяц (написанный или сокращенный).</span><span class="sxs-lookup"><span data-stu-id="3ad5d-132">Day of the month, two or four-digit year, and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="3ad5d-133">21 1932 января</span><span class="sxs-lookup"><span data-stu-id="3ad5d-133">21 1932 January</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ad5d-134">[гг] гг понедельник [TH] дд</span><span class="sxs-lookup"><span data-stu-id="3ad5d-134">[yy]yy Mon[th] dd</span></span></td>
<td><span data-ttu-id="3ad5d-135">Два или четыре цифры года, месяц (написанный или сокращенный) и день.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-135">Two or four-digit year, month (either spelled-out or abbreviated in three letters), and day.</span></span><br/> <dl> <span data-ttu-id="3ad5d-136">1932 января 21 года</span><span class="sxs-lookup"><span data-stu-id="3ad5d-136">1932 January 21</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ad5d-137">гггг мес. [TH]</span><span class="sxs-lookup"><span data-stu-id="3ad5d-137">yyyy Mon[th]</span></span></td>
<td><span data-ttu-id="3ad5d-138">Год и месяц, состоящие из двух или четырех цифр (либо слова, либо сокращения в трех буквах).</span><span class="sxs-lookup"><span data-stu-id="3ad5d-138">Two or four-digit year and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="3ad5d-139">1932 Jan</span><span class="sxs-lookup"><span data-stu-id="3ad5d-139">1932 Jan</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ad5d-140">гггг дд мес. [TH]</span><span class="sxs-lookup"><span data-stu-id="3ad5d-140">yyyy dd Mon[th]</span></span></td>
<td><span data-ttu-id="3ad5d-141">Два или четыре цифры, год, день и месяц (с написанием или сокращением по трем буквам).</span><span class="sxs-lookup"><span data-stu-id="3ad5d-141">Two or four-digit year, day, and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="3ad5d-142">1932 21 января</span><span class="sxs-lookup"><span data-stu-id="3ad5d-142">1932 21 January</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ad5d-143">Пн M {/-.} дд {/-.} [гг] гг</span><span class="sxs-lookup"><span data-stu-id="3ad5d-143">[M]M{/-.}dd{/-.}[yy]yy</span></span></td>
<td><span data-ttu-id="3ad5d-144">Месяц, день и два или четыре цифры года.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-144">Month, day, and two or four-digit year.</span></span> <span data-ttu-id="3ad5d-145">Обратите внимание, что разделители должны быть одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-145">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ad5d-146">дд {/-.} Пн M {/-.} [гг] гг</span><span class="sxs-lookup"><span data-stu-id="3ad5d-146">dd{/-.}[M]M{/-.}[yy]yy</span></span></td>
<td><span data-ttu-id="3ad5d-147">День месяца, месяца и двух или четырех цифр года.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-147">Day of the month, month, and two or four-digit year.</span></span> <span data-ttu-id="3ad5d-148">Обратите внимание, что разделители должны быть одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-148">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ad5d-149">Пн M {/-.} [гг] гг {/-.} DDL</span><span class="sxs-lookup"><span data-stu-id="3ad5d-149">[M]M{/-.}[yy]yy{/-.}dd</span></span></td>
<td><span data-ttu-id="3ad5d-150">Месяц, два или четыре цифры, год и день.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-150">Month, two or four-digit year, and day.</span></span> <span data-ttu-id="3ad5d-151">Обратите внимание, что разделители должны быть одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-151">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ad5d-152">дд {/-.} [гг] гг {/-.} Пн Пн</span><span class="sxs-lookup"><span data-stu-id="3ad5d-152">dd{/-.}[yy]yy{/-.}[M]M</span></span></td>
<td><span data-ttu-id="3ad5d-153">День месяца, два или четыре цифры, год и месяц.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-153">Day of the month, two or four-digit year, and month.</span></span> <span data-ttu-id="3ad5d-154">Обратите внимание, что разделители должны быть одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-154">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ad5d-155">[гг] гг {/-.} дд {/-.} Пн Пн</span><span class="sxs-lookup"><span data-stu-id="3ad5d-155">[yy]yy{/-.}dd{/-.}[M]M</span></span></td>
<td><span data-ttu-id="3ad5d-156">Два или четыре цифры, год, день и месяц.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-156">Two or four digit year, day, and month.</span></span> <span data-ttu-id="3ad5d-157">Обратите внимание, что разделители должны быть одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-157">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ad5d-158">[гг] гг {/-.} Пн M {/-.} DDL</span><span class="sxs-lookup"><span data-stu-id="3ad5d-158">[yy]yy{/-.}[M]M{/-.}dd</span></span></td>
<td><span data-ttu-id="3ad5d-159">Два или четыре цифры, год, месяц и день.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-159">Two or four digit year, month, and day.</span></span> <span data-ttu-id="3ad5d-160">Обратите внимание, что разделители должны быть одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-160">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ad5d-161">[гг] yyMMdd</span><span class="sxs-lookup"><span data-stu-id="3ad5d-161">[yy]yyMMdd</span></span></td>
<td><span data-ttu-id="3ad5d-162">Два или четыре цифры, год, месяц и день без пробелов.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-162">Two or four digit year, month, and day, without spaces.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ad5d-163">yyyy [дд]]</span><span class="sxs-lookup"><span data-stu-id="3ad5d-163">yyyy[MM[dd]]</span></span></td>
<td><span data-ttu-id="3ad5d-164">Два или четыре цифры, необязательный месяц и дополнительный день без пробелов.</span><span class="sxs-lookup"><span data-stu-id="3ad5d-164">Two or four digit year, optional month, and optional day, without spaces.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="3ad5d-165">См. также</span><span class="sxs-lookup"><span data-stu-id="3ad5d-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ad5d-166">Предложения WHERE</span><span class="sxs-lookup"><span data-stu-id="3ad5d-166">WHERE Clause</span></span>](where-clause.md)
</dt> </dl>

 

 




