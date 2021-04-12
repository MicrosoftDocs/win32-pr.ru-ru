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
# <a name="locale_return-constants"></a>\_Константы возврата языкового стандарта \*

В этом разделе определяются константы, возвращаемые языковым стандартом, которые \_ \* используются в NLS.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Значение</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LOCALE_RETURN_GENITIVE_NAMES</td>
<td><strong>Windows 7 и более поздние версии:</strong> Получение имен женитиве месяцев, которые используются, когда названия месяцев объединяются с другими элементами. Например, в украинский эквивалентом Январь записывается &quot; січень, &quot; когда месяц именуется только один раз. Однако если название месяца используется в сочетании, например, в дате, например 5 января 2003, используется женитиве форма имени. Для примера "Украинский" название месяца женитиве отображается как &quot; 5 січня 2003 &quot; . Список названий месяцев женитиве начинается с января и разделяются точками с запятой. Если нет 13-го месяца, используйте точку с запятой в конце списка.
<blockquote>
[!Note]<br />
Названия месяцев женитиве не существуют на всех языках.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>LOCALE_RETURN_NUMBER</td>
<td><strong>Windows Me/98, Windows NT 4,0 и более поздние версии:</strong> Получение числа. Эта константа заставляет <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> или <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> извлечь значение как число, а не как строку. Буфер, принимающий значение, должен быть не меньше длины значения DWORD. Эту константу можно сочетать с любой другой константой, имя которой начинается с &quot; LOCALE_I &quot; .</td>
</tr>
</tbody>
</table>



 

 

 




