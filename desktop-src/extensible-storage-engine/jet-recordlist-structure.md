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
ms.openlocfilehash: 983a0d6a73d4a3bb5e44095f46cc52d537ce15f3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465101"
---
# <a name="jet_recordlist-structure"></a>Структура JET_RECORDLIST


_**Применимо к:** Windows | Windows Сервером_

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


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетклосетабле](./jetclosetable-function.md)  
[жетинтерсектиндексес](./jetintersectindexes-function.md)  
[жетроллбакк](./jetrollback-function.md)
