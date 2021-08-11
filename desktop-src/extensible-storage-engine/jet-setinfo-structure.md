---
description: 'Дополнительные сведения: структура JET_SETINFO'
title: Структура JET_SETINFO
TOCTitle: JET_SETINFO Structure
ms:assetid: cbc41175-e48f-46b0-aeb1-1120fa2cd981
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294090(v=EXCHG.10)
ms:contentKeyID: 32765705
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
ms.openlocfilehash: 379fd60a001312152dbe181c27a3e8158ceca79b4cfa9075a530b6c73f4337cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118253445"
---
# <a name="jet_setinfo-structure"></a>Структура JET_SETINFO


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_setinfo-structure"></a>Структура JET_SETINFO

Структура **JET_SETINFO** содержит необязательные входные параметры для [жетсетколумн](./jetsetcolumn-function.md). Указатель **null** можно передать, где в противном случае будет передан указатель на эту структуру. Значение передачи **значения NULL** аналогично передаче **JET_SETINFO** с параметром **кбструкт** , равным sizeof (JET_SETINFO), **иблонгвалуе** имеет значение 0 (ноль), а **итагсекуенце** — значение 1.

```cpp
typedef struct {
  unsigned long cbStruct;
  unsigned long ibLongValue;
  unsigned long itagSequence;
} JET_SETINFO;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер **JET_SETINFO** в байтах. Это значение подтверждает наличие следующих полей.

**иблонгвалуе**

Смещение к первому байту, заданному в столбце типа [JET_coltypLongBinary](./jet-coltyp.md) или [JET_coltypLongText](./jet-coltyp.md).

**итагсекуенце**

Описывает порядковый номер значения в столбце с несколькими значениями, который необходимо задать. Массив значений является исходным. Первое значение — Sequence 1, а не 0 (ноль). Если столбец записи имеет только одно значение, то значение 1 должно передаваться как **итагсекуенце** при замене этого значения. Значение 0 (ноль) означает, что новый экземпляр значения столбца добавляется в конец последовательности значений столбцов.

При использовании столбца, который может содержать несколько значений, в [жетсетколумн](./jetsetcolumn-function.md)можно использовать только порядковый номер больше 1 в [жетсетколумн](./jetsetcolumn-function.md) и [жетретриевеколумн](./jetretrievecolumn-function.md) или 0. В текущей реализации обработчика любой столбец, созданный с помощью JET_bitColumnTagged, может содержать несколько значений. Столбцы, созданные JET_bitColumnMultiValued, отличаются от столбцов с многозначными тегами только тем способом, в котором они индексируются. Дополнительные сведения см. в разделе [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

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
<td><p><strong>Server</strong></p></td>
<td><p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также:

[жетсетколумн](./jetsetcolumn-function.md)
