---
description: Ряд фактоидс описывают входные данные, которые являются общими для всех распознавателей языков и не должны иметь различных форматов для разных языков. В следующей таблице перечислены фактоидс, общие для всех языков.
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: Фактоидс, общие для разных языков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1faefbb9991562535f711f867c45bd614c595941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701611"
---
# <a name="factoids-common-across-languages"></a><span data-ttu-id="35bd9-104">Фактоидс, общие для разных языков</span><span class="sxs-lookup"><span data-stu-id="35bd9-104">Factoids Common Across Languages</span></span>

<span data-ttu-id="35bd9-105">Ряд фактоидс описывают входные данные, которые являются общими для всех распознавателей языков и не должны иметь различных форматов для разных языков.</span><span class="sxs-lookup"><span data-stu-id="35bd9-105">A number of factoids describe input that is common to all language recognizers and need not have different formats for different languages.</span></span> <span data-ttu-id="35bd9-106">В следующей таблице перечислены фактоидс, общие для всех языков.</span><span class="sxs-lookup"><span data-stu-id="35bd9-106">The following table lists factoids that are common across all languages.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35bd9-107">фактоид</span><span class="sxs-lookup"><span data-stu-id="35bd9-107">Factoid</span></span></th>
<th><span data-ttu-id="35bd9-108">Определение</span><span class="sxs-lookup"><span data-stu-id="35bd9-108">Definition</span></span></th>
<th><span data-ttu-id="35bd9-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="35bd9-109">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35bd9-110"><strong>Число</strong></span><span class="sxs-lookup"><span data-stu-id="35bd9-110"><strong>Digit</strong></span></span></td>
<td><span data-ttu-id="35bd9-111">Задает сдвиг для одной цифры.</span><span class="sxs-lookup"><span data-stu-id="35bd9-111">Sets bias for a single digit.</span></span> <span data-ttu-id="35bd9-112">Распознаватель перемещается в сторону возврата только отдельных цифр, если задано значение фактоид.</span><span class="sxs-lookup"><span data-stu-id="35bd9-112">The recognizer is biased toward returning only single digits when this factoid is set.</span></span><br/></td>
<td><span data-ttu-id="35bd9-113">0-9</span><span class="sxs-lookup"><span data-stu-id="35bd9-113">0-9</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35bd9-114"><strong>Электронная почта</strong></span><span class="sxs-lookup"><span data-stu-id="35bd9-114"><strong>Email</strong></span></span></td>
<td><span data-ttu-id="35bd9-115">Задает смещение адреса электронной почты.</span><span class="sxs-lookup"><span data-stu-id="35bd9-115">Sets bias for an email address.</span></span><br/></td>
<td>someone@example.com<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35bd9-116"><strong>Web</strong></span><span class="sxs-lookup"><span data-stu-id="35bd9-116"><strong>Web</strong></span></span></td>
<td><span data-ttu-id="35bd9-117">Задает смещение для различных форматов URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="35bd9-117">Sets bias for various URL formats.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="35bd9-118">Параметры по умолчанию для распознавателя включают в себя <strong>веб-</strong> фактоид.</span><span class="sxs-lookup"><span data-stu-id="35bd9-118">The default settings for the recognizer include the <strong>Web</strong> factoid.</span></span> <span data-ttu-id="35bd9-119">По этой причине вы не можете заметить значительную разницу между <strong>веб-</strong> фактоид и параметром по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="35bd9-119">Because of this, you may not notice a large difference between the <strong>Web</strong> factoid and the default setting.</span></span> <span data-ttu-id="35bd9-120">Однако <strong>веб-</strong> фактоид помогает избежать пробелов между словами в URL-адресе.</span><span class="sxs-lookup"><span data-stu-id="35bd9-120">However, the <strong>Web</strong> factoid does help eliminate spaces between words in a URL.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="35bd9-121">http: \\ Microsoft.NET</span><span class="sxs-lookup"><span data-stu-id="35bd9-121">http:\\microsoft.net</span></span><br/> https://microsoft.us/<br/> <span data-ttu-id="35bd9-122">HTTPS: \\ www.Microsoft.au </span><span class="sxs-lookup"><span data-stu-id="35bd9-122">https:\\www.microsoft.au</span></span>\<br/> https://microsoft.com<br/> <span data-ttu-id="35bd9-123">www.microsoft_world. com</span><span class="sxs-lookup"><span data-stu-id="35bd9-123">www.microsoft_world.com</span></span><br/> <span data-ttu-id="35bd9-124">www.microsoft.us </span><span class="sxs-lookup"><span data-stu-id="35bd9-124">www.microsoft.us</span></span>\<br/> <span data-ttu-id="35bd9-125">http: \\www.microsoft.com\myfile.htm</span><span class="sxs-lookup"><span data-stu-id="35bd9-125">http:\\www.microsoft.com\myfile.htm</span></span><br/> <span data-ttu-id="35bd9-126">http: \\www.microsoft.com\myfile.html</span><span class="sxs-lookup"><span data-stu-id="35bd9-126">http:\\www.microsoft.com\myfile.html</span></span><br/> <span data-ttu-id="35bd9-127">http: \\ www. Microsoft. ком\мифиле.АСП</span><span class="sxs-lookup"><span data-stu-id="35bd9-127">http:\\www.microsoft.com\myfile.asp</span></span><br/> <span data-ttu-id="35bd9-128">http: \\ www.Microsoft.UK</span><span class="sxs-lookup"><span data-stu-id="35bd9-128">http:\\www.microsoft.uk</span></span><br/> <span data-ttu-id="35bd9-129">http: \\ www.Microsoft.info</span><span class="sxs-lookup"><span data-stu-id="35bd9-129">http:\\www.microsoft.info</span></span><br/> <span data-ttu-id="35bd9-130">www.microsoft.biz</span><span class="sxs-lookup"><span data-stu-id="35bd9-130">www.microsoft.biz</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35bd9-131"><strong>По умолчанию</strong></span><span class="sxs-lookup"><span data-stu-id="35bd9-131"><strong>Default</strong></span></span></td>
<td><span data-ttu-id="35bd9-132">Возвращает распознаватель в параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="35bd9-132">Returns the recognizer to its default settings.</span></span><br/></td>
<td><span data-ttu-id="35bd9-133">Значение по умолчанию для фактоидс для западных языков включает системный словарь, Пользовательский словарь, различные знаки препинания, а также <strong>веб-</strong> Фактоидс и <strong>Number</strong> .</span><span class="sxs-lookup"><span data-stu-id="35bd9-133">The default setting for factoids for western languages includes the system dictionary, user dictionary, various punctuations, and the <strong>Web</strong> and <strong>Number</strong> factoids.</span></span><br/> <span data-ttu-id="35bd9-134">Значение по умолчанию для фактоидс для восточно-азиатских языков включает все символы, поддерживаемые распознавателем.</span><span class="sxs-lookup"><span data-stu-id="35bd9-134">The default setting for factoids for East Asian languages includes all characters supported by the recognizer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35bd9-135"><strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="35bd9-135"><strong>None</strong></span></span></td>
<td><span data-ttu-id="35bd9-136">Отключает все фактоидс, словари и языковую модель.</span><span class="sxs-lookup"><span data-stu-id="35bd9-136">Disables all factoids, dictionaries, and the language model.</span></span><br/></td>
<td><span data-ttu-id="35bd9-137">Этот фактоид следует использовать, только если вы не хотите, чтобы распознаватель использовал грамматические правила или словари, включая системный словарь.</span><span class="sxs-lookup"><span data-stu-id="35bd9-137">This factoid should be used only when you do not want the recognizer to use any grammar rules or dictionaries, including the system dictionary.</span></span> <span data-ttu-id="35bd9-138">Этот фактоид полезен для ввода случайных строк, таких как коды продуктов.</span><span class="sxs-lookup"><span data-stu-id="35bd9-138">This factoid is useful for input of random strings such as product codes.</span></span> <span data-ttu-id="35bd9-139">Не используйте флаг приведение к этому фактоид.</span><span class="sxs-lookup"><span data-stu-id="35bd9-139">Do not use the Coerce flag with this factoid.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




