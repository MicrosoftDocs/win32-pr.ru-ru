---
description: 'Дополнительные сведения: структура JET_RECORDLIST'
title: Структура JET_RECORDLIST
TOCTitle: JET_RECORDLIST Structure
ms:assetid: 6b4d97a0-4b42-4f7c-bb18-b6db3c92668a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269287(v=EXCHG.10)
ms:contentKeyID: 32765579
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
ms.openlocfilehash: 16aca3a13bbae7c61bfe03aca49acea775820d39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912991"
---
# <a name="jet_recordlist-structure"></a>Структура JET_RECORDLIST


_**Применимо к:** Windows | Windows Server_

## <a name="jet_recordlist-structure"></a>Структура JET_RECORDLIST

Структура **JET_RECORDLIST** находит записи, находящиеся в пересечении указанных диапазонов индексов, когда они используются с функцией [жетинтерсектиндексес](./jetintersectindexes-function.md) .

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidBookmark;
    } JET_RECORDLIST;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер структуры **JET_RECORDLIST** в байтах.

**TableID**

Идентификатор таблицы временной таблицы, содержащей закладки для результатов запроса. Таблица будет автоматически закрыта при откате текущей транзакции с помощью [жетроллбакк](./jetrollback-function.md); в противном случае он должен быть закрыт с помощью [жетклосетабле](./jetclosetable-function.md).

**крекорд**

Количество строк во временной таблице.

**колумнидбукмарк**

Идентификатор столбца закладки во временной таблице.

### <a name="remarks"></a>Комментарии

Временная таблица, идентифицируемая **tableid** , имеет один столбец. Этот один столбец содержит закладки, и каждая запись должна помещаться в буфер размером JET_cbBookmarkMost байт.

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

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетклосетабле](./jetclosetable-function.md)  
[жетинтерсектиндексес](./jetintersectindexes-function.md)  
[жетроллбакк](./jetrollback-function.md)
