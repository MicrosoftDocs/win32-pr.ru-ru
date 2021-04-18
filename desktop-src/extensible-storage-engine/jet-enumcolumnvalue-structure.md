---
description: 'Дополнительные сведения: структура JET_ENUMCOLUMNVALUE'
title: Структура JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE Structure
ms:assetid: a9882d7b-0c53-4a5d-bc98-0979e6e68c88
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294052(v=EXCHG.10)
ms:contentKeyID: 32765652
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
ms.openlocfilehash: bc95c6b8403a64432451ea29dbb66868fad25264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693436"
---
# <a name="jet_enumcolumnvalue-structure"></a>Структура JET_ENUMCOLUMNVALUE


_**Применимо к:** Windows | Windows Server_

## <a name="jet_enumcolumnvalue-structure"></a>Структура JET_ENUMCOLUMNVALUE

Структура **JET_ENUMCOLUMNVALUE** перечисляет значения столбцов записи с помощью функции [жетенумератеколумнс](./jetenumeratecolumns-function.md) . [Жетенумератеколумнс](./jetenumeratecolumns-function.md) возвращает массив структур **JET_ENUMCOLUMNVALUE** . Массив возвращается в памяти, выделенной с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено этой функции.

```cpp
    typedef struct {
      unsigned long itagSequence;
      JET_ERR err;
      unsigned long cbData;
      void* pvData;
    } JET_ENUMCOLUMNVALUE;
```

### <a name="members"></a>Элементы

**итагсекуенце**

Значение столбца (по основанному на единицу индексу), которое было перечислено.

**Err**

Код состояния столбца, полученный в результате перечисления значения столбца.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_wrnColumnNull</p></td>
<td><p>Запрошенное значение столбца равно NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSkipped</p></td>
<td><p><em>Итагсекуенце</em> , указанный в элементе массива <em>ргтагсекуенце</em> в структуре <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> , соответствующей этой <strong>JET_ENUMCOLUMNVALUE</strong> структуре, была нулевой.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnTruncated</p></td>
<td><p>Значение запрошенного столбца было усечено до указанного размера перед возвратом.</p>
<p>Это усечение происходит только для длинных текстовых и длинных двоичных столбцов, содержащих большие объемы данных.</p></td>
</tr>
</tbody>
</table>


**cbData**

Значение столбца, перечисленное для столбца.

Выходной буфер возвращается в память, которая была выделена с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено в [жетенумератеколумнс](./jetenumeratecolumns-function.md).

**пвдата**

Значение столбца, перечисленное для столбца.

Выходной буфер возвращается в память, которая была выделена с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено в [жетенумератеколумнс](./jetenumeratecolumns-function.md).

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

[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE]()  
[JET_ERR](./jet-err.md)  
[жетенумератеколумнс](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
