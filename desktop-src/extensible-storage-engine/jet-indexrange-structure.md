---
description: 'Дополнительные сведения: структура JET_INDEXRANGE'
title: Структура JET_INDEXRANGE
TOCTitle: JET_INDEXRANGE Structure
ms:assetid: 8e437f7d-1e21-4a0b-a5a5-1c78235a4f80
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269335(v=EXCHG.10)
ms:contentKeyID: 32765624
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
ms.openlocfilehash: 48e9da5822f69d4460a1699252112899a990188d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470880"
---
# <a name="jet_indexrange-structure"></a>Структура JET_INDEXRANGE


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_indexrange-structure"></a>Структура JET_INDEXRANGE

Структура **JET_INDEXRANGE** определяет диапазон индексов при использовании с функцией [жетинтерсектиндексес](./jetintersectindexes-function.md) .

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      JET_GRBIT grbit;
    } JET_INDEXRANGE;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер **JET_INDEXRANGE** в байтах.

**TableID**

Курсор, для которого ранее был задан диапазон индексов с [жетсетиндексранже](./jetsetindexrange-function.md).

**грбит**

Битовая маска, состоящая только из одного из следующих элементов.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitRecordInIndex</p> | <p>Указывает, что диапазон индекса должен обрабатываться обычным образом.</p> | 
| <p>JET_bitRecordNotInIndex</p> | <p>Зарезервировано для последующего использования. Не используйте.</p> | 



### <a name="remarks"></a>Комментарии

Каждая **JET_INDEXRANGE** структура, передаваемая в [жетинтерсектиндексес](./jetintersectindexes-function.md) , представляет диапазон индекса, который будет пересекаться вызовом API. Для курсора, заданного в **JET_INDEXRANGE** , должен быть уже установлен допустимый диапазон индексов с успешным вызовом [жетсетиндексранже](./jetsetindexrange-function.md).

### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетклосетабле](./jetclosetable-function.md)  
[жетинтерсектиндексес](./jetintersectindexes-function.md)  
[жетсетиндексранже](./jetsetindexrange-function.md)
