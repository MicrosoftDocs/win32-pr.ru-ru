---
description: 'Дополнительные сведения: структура JET_ENUMCOLUMN'
title: Структура JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN Structure
ms:assetid: f8f512fd-5fcf-47ed-a5db-2fb3bd76c2d7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294138(v=EXCHG.10)
ms:contentKeyID: 32765752
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
ms.openlocfilehash: 6ac89a45e37631b554fc7b2dc28266c95cfae3fba54debb427abfd8db621ea3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118766092"
---
# <a name="jet_enumcolumn-structure"></a>Структура JET_ENUMCOLUMN


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_enumcolumn-structure"></a>Структура JET_ENUMCOLUMN

Структура **JET_ENUMCOLUMN** перечисляет значения столбцов записи a при использовании функции [жетенумератеколумнс](./jetenumeratecolumns-function.md) . [Жетенумератеколумнс](./jetenumeratecolumns-function.md) возвращает массив структур **JET_ENUMCOLUMN** . Массив возвращается в памяти, выделенной с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено этому API.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      JET_ERR err;
      union {
        struct {
          unsigned long cEnumColumnValue;
          JET_ENUMCOLUMNVALUE rgEnumColumnValue;
        };
        struct {
          unsigned long cbData;
          void* pvData;
        };
      };
    } JET_ENUMCOLUMN;
```

### <a name="members"></a>Элементы

**columnid**

Идентификатор столбца, который был перечислен.

**Err**

Код состояния столбца, полученный в результате перечисления столбца.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Коды ошибок</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errBadColumnId</p></td>
<td><p>Идентификатор столбца находится за пределами допустимых ограничений идентификатора столбца.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Столбец, описываемый ИДЕНТИФИКАТОРом столбца, не существует в таблице.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull</p></td>
<td><p>Все значения для этого столбца равны NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnPresent</p></td>
<td><p>Указан JET_bitEnumeratePresenceOnly, и для этого столбца было возвращено по крайней мере одно значение столбца, отличное от NULL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSingleValue</p></td>
<td><p>Указан JET_bitEnumerateCompressOutput, и для этого столбца возвращено ровно одно значение столбца, отличное от NULL. В результате возвращается сжатая форма <strong>JET_ENUMCOLUMN</strong> . Дополнительные сведения см. в разделе <strong>JET_ENUMCOLUMN</strong> .</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSkipped</p></td>
<td><p>Идентификатор столбца в структуре <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> , соответствующей этой <strong>JET_ENUMCOLUMN</strong> структуре, равен нулю.</p></td>
</tr>
</tbody>
</table>


**ценумколумнвалуе**

Массив значений столбца, перечисленных для столбца. Выходной буфер возвращается в память, которая была выделена с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено в [жетенумератеколумнс](./jetenumeratecolumns-function.md).

Этот выходной буфер используется, когда код состояния столбца не равен JET_wrnColumnSingleValue. Дополнительные сведения см. в разделе [жетенумератеколумнс](./jetenumeratecolumns-function.md).

Возвращается, если "Err \! = JET_wrnColumnSingleValue".

**рженумколумнвалуе**

Массив значений столбца, перечисленных для столбца. Выходной буфер возвращается в память, которая была выделена с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено в [жетенумератеколумнс](./jetenumeratecolumns-function.md).

Этот выходной буфер используется, когда код состояния столбца не равен JET_wrnColumnSingleValue. Дополнительные сведения см. в разделе [жетенумератеколумнс](./jetenumeratecolumns-function.md).

Возвращается, если "Err \! = JET_wrnColumnSingleValue".

**cbData**

Значение столбца, перечисленное для столбца.

Выходной буфер возвращается в память, которая была выделена с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено в [жетенумератеколумнс](./jetenumeratecolumns-function.md).

Этот выходной буфер используется только в том случае, если код состояния столбца имеет значение JET_wrnColumnSingleValue. Дополнительные сведения см. в разделе [жетенумератеколумнс](./jetenumeratecolumns-function.md).

Возвращается, если "Err = = JET_wrnColumnSingleValue".

**пвдата**

Значение столбца, перечисленное для столбца.

Выходной буфер возвращается в память, которая была выделена с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено в [жетенумератеколумнс](./jetenumeratecolumns-function.md).

Этот выходной буфер используется только в том случае, если код состояния столбца имеет значение JET_wrnColumnSingleValue. Дополнительные сведения см. в разделе [жетенумератеколумнс](./jetenumeratecolumns-function.md).

Возвращается, если "Err = = JET_wrnColumnSingleValue".

### <a name="requirements"></a>Requirements (Требования)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Сервер</strong></p></td>
<td><p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_ENUMCOLUMNID](./jet-enumcolumnid-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[жетенумератеколумнс](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
