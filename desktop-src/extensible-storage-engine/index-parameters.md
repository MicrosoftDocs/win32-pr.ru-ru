---
description: 'Дополнительные сведения: параметры индекса'
title: Параметры индекса
TOCTitle: Index Parameters
ms:assetid: df3dfbc7-71fb-4ae2-a94a-b00eaa1572ec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294119(v=EXCHG.10)
ms:contentKeyID: 32765733
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2901887233ff8b25114334c97e6a731072a69ce1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081548"
---
# <a name="index-parameters"></a>Параметры индекса


_**Применимо к:** Windows | Windows Server_

## <a name="index-parameters"></a>Параметры индекса

Этот раздел содержит параметры, используемые для индекса.

*JET_paramIndexTupleIncrement*  
132  

Этот параметр задает значение по умолчанию для шага смещения, используемого для пошагового перехода к значению исходного столбца при создании каждого кортежа. Дополнительные сведения см. в разделе Структура [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>0 - 32767</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Экземпляр</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на физический макет:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на надежность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на производительность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Windows Vista и более поздние версии</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTupleStart*  
133  

Этот параметр задает значение по умолчанию для смещения в значении исходного столбца, с которого начнется создание кортежей. Дополнительные сведения см. в разделе Структура [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>0 - 32767</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Экземпляр</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на физический макет:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на надежность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на производительность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Windows Vista и более поздние версии</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesLengthMax*  
111  

Этот параметр задает значение по умолчанию для максимальной длины кортежа в индексе кортежа. Дополнительные сведения см. в разделе Структура [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

**Windows Vista:**  До выхода Windows Vista установка этого параметра в нулевое значение применяет его к значению по умолчанию. Для Windows Vista это больше не поддерживается.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>10</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p><strong>Windows 2000, Windows XP и Windows Server 2003: </strong>  0, 2-255</p>
<p><strong>Windows Vista:</strong>  2-255</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Экземпляр</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на физический макет:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на надежность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на производительность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Windows XP и более поздние версии</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesLengthMin*  
110  

Этот параметр задает значение по умолчанию для минимальной длины кортежа в индексе кортежа. Дополнительные сведения см. в разделе [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

**Windows Vista:**  До выхода Windows Vista установка этого параметра в нулевое значение применяет его к значению по умолчанию. Для Windows Vista это больше не поддерживается.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p><strong>Windows 2000, Windows XP и Windows Server 2003: </strong>  0, 2-255</p>
<p><strong>Windows Vista:</strong>  2-255</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Экземпляр</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на физический макет:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на надежность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на производительность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Windows XP и более поздние версии</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesToIndexMax*  
112  

Этот параметр задает значение по умолчанию для максимальной длины исходной строки, которая должна быть разбита на кортежи для индекса кортежа. Дополнительные сведения см. в разделе [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

**Windows Vista:**  До выхода Windows Vista установка этого параметра в нулевое значение применяет его к значению по умолчанию. Для Windows Vista это больше не поддерживается.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>32767</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p><strong>Windows 2000, Windows XP и Windows Server 2003:</strong>  0 – 32767</p>
<p><strong>Windows Vista:</strong>  1 – 32767</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Экземпляр</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на физический макет:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на надежность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на производительность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Windows XP и более поздние версии</p></td>
</tr>
</tbody>
</table>


*JET_paramUnicodeIndexDefault*  
72  

Этот параметр управляет параметрами Юникода по умолчанию, используемыми любым индексом для ключевого столбца Юникода. Тип этого параметра — [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) и фактически передается с помощью указателя буфера, хранящегося в целочисленном параметре [жетжетсистемпараметер](./jetgetsystemparameter-function.md) и [жетсетсистемпараметер](./jetsetsystemparameter-function.md). Размер буфера должен равняться размеру [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) и должен передаваться в [жетжетсистемпараметер](./jetgetsystemparameter-function.md) с помощью параметра размера буфера строки. Это явное несоответствие, но это поведение этого параметра.

Значение этого параметра по умолчанию содержит код языка для английского языка (США) и следующие флаги [лкмапстрингв](/windows/win32/api/winnls/nf-winnls-lcmapstringa): LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE и NORM_IGNOREWIDTH.

**Windows 2000:**  СОРТИД в LCID игнорируется. Всегда используется СОРТИД SORT_DEFAULT.

**Windows 2000:**  Флаги [лкмапстрингв](/windows/win32/api/winnls/nf-winnls-lcmapstringa) должны содержать следующие флаги: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE и NORM_IGNOREWIDTH. Кроме того, флаги [лкмапстрингв](/windows/win32/api/winnls/nf-winnls-lcmapstringa)могут содержать следующие флаги: NORM_IGNORENONSPACE.

**Примечание**  .  Если приложению требуется хранить данные в Юникоде, настоятельно рекомендуется не полагаться на параметры Юникода по умолчанию для индексов. Использование языка "Английский (США)" — запереть использования инвариантного языкового стандарта, и флаги [лкмапстрингв](/windows/win32/api/winnls/nf-winnls-lcmapstringa)по умолчанию могут серьезно мешать работе некоторых языков. Необходимо всегда указывать собственные параметры для параметров Юникода в JetCreateIndex2 с помощью [JET_INDEXCREATE](./jet-indexcreate-structure.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>Специальные функции</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>JET_UNICODEINDEX * (JET_UNICODEINDEX)</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>Специальные функции</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Экземпляр</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на физический макет:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на надежность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на производительность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Все</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также:

[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[жеткреатеинстанце](./jetcreateinstance-function.md)  
[жетжетсистемпараметер](./jetgetsystemparameter-function.md)  
[жетинит](./jetinit-function.md)  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)
