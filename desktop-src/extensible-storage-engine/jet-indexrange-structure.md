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
ms.openlocfilehash: b5b68e7ebf6df39757ab39947201b945e35a3ece85518a3cb202525033cdd214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118485602"
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
<td><p>JET_bitRecordInIndex</p></td>
<td><p>Указывает, что диапазон индекса должен обрабатываться обычным образом.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecordNotInIndex</p></td>
<td><p>Зарезервировано для последующего использования. Не используйте.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Remarks

Каждая **JET_INDEXRANGE** структура, передаваемая в [жетинтерсектиндексес](./jetintersectindexes-function.md) , представляет диапазон индекса, который будет пересекаться вызовом API. Для курсора, заданного в **JET_INDEXRANGE** , должен быть уже установлен допустимый диапазон индексов с успешным вызовом [жетсетиндексранже](./jetsetindexrange-function.md).

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

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетклосетабле](./jetclosetable-function.md)  
[жетинтерсектиндексес](./jetintersectindexes-function.md)  
[жетсетиндексранже](./jetsetindexrange-function.md)
