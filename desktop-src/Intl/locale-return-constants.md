---
description: '\_Константы возврата языкового стандарта \*'
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: Константы LOCALE_RETURN *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d3e5017a6463457b7bc36358e9956365430c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272068"
---
# <a name="locale_return-constants"></a><span data-ttu-id="802c5-103">\_Константы возврата языкового стандарта \*</span><span class="sxs-lookup"><span data-stu-id="802c5-103">LOCALE\_RETURN\* Constants</span></span>

<span data-ttu-id="802c5-104">В этом разделе определяются константы, возвращаемые языковым стандартом, которые \_ \* используются в NLS.</span><span class="sxs-lookup"><span data-stu-id="802c5-104">This topic defines the LOCALE\_RETURN\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="802c5-105">Значение</span><span class="sxs-lookup"><span data-stu-id="802c5-105">Value</span></span></th>
<th><span data-ttu-id="802c5-106">Значение</span><span class="sxs-lookup"><span data-stu-id="802c5-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="802c5-107">LOCALE_RETURN_GENITIVE_NAMES</span><span class="sxs-lookup"><span data-stu-id="802c5-107">LOCALE_RETURN_GENITIVE_NAMES</span></span></td>
<td><span data-ttu-id="802c5-108"><strong>Windows 7 и более поздние версии:</strong> Получение имен женитиве месяцев, которые используются, когда названия месяцев объединяются с другими элементами.</span><span class="sxs-lookup"><span data-stu-id="802c5-108"><strong>Windows 7 and later:</strong> Retrieve the genitive names of months, which are the names used when the month names are combined with other items.</span></span> <span data-ttu-id="802c5-109">Например, в украинский эквивалентом Январь записывается &quot; січень, &quot; когда месяц именуется только один раз.</span><span class="sxs-lookup"><span data-stu-id="802c5-109">For example, in Ukrainian the equivalent of January is written &quot;Січень&quot; when the month is named alone.</span></span> <span data-ttu-id="802c5-110">Однако если название месяца используется в сочетании, например, в дате, например 5 января 2003, используется женитиве форма имени.</span><span class="sxs-lookup"><span data-stu-id="802c5-110">However, when the month name is used in combination, for example, in a date such as January 5th, 2003, the genitive form of the name is used.</span></span> <span data-ttu-id="802c5-111">Для примера "Украинский" название месяца женитиве отображается как &quot; 5 січня 2003 &quot; .</span><span class="sxs-lookup"><span data-stu-id="802c5-111">For the Ukrainian example, the genitive month name is displayed as &quot;5 січня 2003&quot;.</span></span> <span data-ttu-id="802c5-112">Список названий месяцев женитиве начинается с января и разделяются точками с запятой.</span><span class="sxs-lookup"><span data-stu-id="802c5-112">The list of genitive month names begins with January and is semicolon-delimited.</span></span> <span data-ttu-id="802c5-113">Если нет 13-го месяца, используйте точку с запятой в конце списка.</span><span class="sxs-lookup"><span data-stu-id="802c5-113">If there is no 13th month, use a semicolon in its place at the end of the list.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="802c5-114">Названия месяцев женитиве не существуют на всех языках.</span><span class="sxs-lookup"><span data-stu-id="802c5-114">Genitive month names do not exist in all languages.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="802c5-115">LOCALE_RETURN_NUMBER</span><span class="sxs-lookup"><span data-stu-id="802c5-115">LOCALE_RETURN_NUMBER</span></span></td>
<td><span data-ttu-id="802c5-116"><strong>Windows Me/98, Windows NT 4,0 и более поздние версии:</strong> Получение числа.</span><span class="sxs-lookup"><span data-stu-id="802c5-116"><strong>Windows Me/98, Windows NT 4.0 and later:</strong> Retrieve a number.</span></span> <span data-ttu-id="802c5-117">Эта константа заставляет <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> или <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> извлечь значение как число, а не как строку.</span><span class="sxs-lookup"><span data-stu-id="802c5-117">This constant causes <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> or <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> to retrieve a value as a number instead of as a string.</span></span> <span data-ttu-id="802c5-118">Буфер, принимающий значение, должен быть не меньше длины значения DWORD.</span><span class="sxs-lookup"><span data-stu-id="802c5-118">The buffer that receives the value must be at least the length of a DWORD value.</span></span> <span data-ttu-id="802c5-119">Эту константу можно сочетать с любой другой константой, имя которой начинается с &quot; LOCALE_I &quot; .</span><span class="sxs-lookup"><span data-stu-id="802c5-119">This constant can be combined with any other constant having a name that begins with &quot;LOCALE_I&quot;.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




