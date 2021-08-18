---
description: 'Дополнительные сведения: структура JET_RETINFO'
title: Структура JET_RETINFO
TOCTitle: JET_RETINFO Structure
ms:assetid: a47a7902-3ecd-4d42-941f-89d25d78eb4c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294049(v=EXCHG.10)
ms:contentKeyID: 32765648
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
ms.openlocfilehash: a04ee087f036bf0d6a9e0bb4c9c558dbfe3ae5a8fc8e875973ef2930e7ba911a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038732"
---
# <a name="jet_retinfo-structure"></a>Структура JET_RETINFO


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_retinfo-structure"></a>Структура JET_RETINFO

Структура **JET_RETINFO** содержит необязательные входные и выходные параметры для [жетретриевеколумн](./jetretrievecolumn-function.md). Указатель NULL можно передать, где в противном случае будет передан указатель на эту структуру. Передача пустого указателя аналогична передаче **JET_RETINFO** с параметром **кбструкт** , для которого задано значение sizeof (JET_RETINFO), **иблонгвалуе** имеет значение 0 (ноль), а **итагсекуенце** — значение 1.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
    } JET_RETINFO;
```

### <a name="members"></a>Элементы

**кбструкт**

Необходимо задать размер структуры **JET_RETINFO** (в байтах) и выполнить для подтверждения наличия следующих полей.

**иблонгвалуе**

Смещение для первого байта, получаемого из столбца типа [JET_coltypLongBinary](./jet-coltyp.md)или [JET_coltypLongText](./jet-coltyp.md). Обратите внимание, что объем данных, извлекаемых с этого смещения, — это Нижняя часть размера выходного буфера и размер данных в фактическом значении после этого смещения.

**итагсекуенце**

Описывает порядковый номер значения в столбце с несколькими значениями. Обратите внимание, что массив значений является исходным. Первое значение — Sequence 1, а не 0. Если столбец записи имеет только одно значение, то в качестве **итагсекуенце** передается 1.

При использовании столбца, который может содержать несколько значений, в [жетсетколумн](./jetsetcolumn-function.md)можно использовать только порядковый номер больше 1 в [жетсетколумн](./jetsetcolumn-function.md) и [жетретриевеколумн](./jetretrievecolumn-function.md) или 0. В текущей реализации обработчика любой столбец, созданный с помощью JET_bitColumnTagged, может содержать несколько значений. Столбцы, созданные JET_bitColumnMultiValued, отличаются от столбцов с многозначными тегами только тем способом, в котором они индексируются. Дополнительные сведения см. в разделе [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

**колумниднексттагжед**

Возвращает значение columnid полученного помеченного, многозначного или разреженного столбца, если все отмеченные столбцы извлекаются путем передачи 0 в качестве значения columnid в [жетретриевеколумн](./jetretrievecolumn-function.md).

### <a name="requirements"></a>Требования

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_RETINFO]()  
[жетретриевеколумн](./jetretrievecolumn-function.md)
