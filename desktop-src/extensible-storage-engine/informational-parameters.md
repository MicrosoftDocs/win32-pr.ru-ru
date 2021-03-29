---
description: 'Подробнее: информационные параметры'
title: Информационные параметры
TOCTitle: Informational Parameters
ms:assetid: 48500fc9-6d89-45b8-92ad-afb997b729f3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269241(v=EXCHG.10)
ms:contentKeyID: 32765543
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
ms.openlocfilehash: a8923b544726e474775684f54fed47d8b4ba281e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811140"
---
# <a name="informational-parameters"></a>Информационные параметры


_**Применимо к:** Windows | Windows Server_

## <a name="informational-parameters"></a>Информационные параметры

Этот раздел содержит параметры, используемые для предоставления сведений о ядре СУБД.

*JET_paramKeyMost*  
134  

Этот параметр только для чтения указывает максимальную допустимую длину ключа индекса, которую можно выбрать для текущего размера страницы базы данных (согласно настройкам JET_paramDatabasePageSize).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>JET_cbKeyMost4KBytePage</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>255 – 65535</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Глобальный</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Н/Д</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Н/Д</p></td>
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
<td><p>Начиная с Windows Server 2008 и Windows Vista</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxColtyp*  
131  

Этот параметр только для чтения возвращает максимальное [JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) для этой версии ядра СУБД. Это значение можно использовать для проверки поддержки определенного [JET_COLTYP](./jet-coltyp.md). Если данный параметр [JET_COLTYP](./jet-coltyp.md) меньше значения этого параметра, он поддерживается ядром СУБД.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>JET_coltypUnsignedShort + 1</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>0 – 255</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Глобальный</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Н/Д</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Н/Д</p></td>
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
<td><p>Начиная с Windows Server 2008 и Windows Vista</p></td>
</tr>
</tbody>
</table>


*JET_paramLVChunkSizeMost*  
163  

Параметр только для чтения, возвращающий размер фрагмента длинных значений на основе настроенного размера страницы. Если длинное значение должно быть считано или записано несколькими вызовами Jet {Set, reby}, то использование буфера с размером, кратным размеру блока, является более эффективным.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>2 КБ страница = 1966 байт<br />
4 КБ страница = 4014 байт<br />
8 КБ страница = 8110 байт<br />
16 КБ страница = 4050 байт<br />
32 КБ страница = 8150 байт</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>0-10000</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Влияет на физический макет:</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Влияет на надежность:</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Влияет на производительность:</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p></p></td>
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
<td><p>Требуется Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также:

[жеткреатеинстанце](./jetcreateinstance-function.md)  
[жетинит](./jetinit-function.md)  
[JET_COLTYP](./jet-coltyp.md)
