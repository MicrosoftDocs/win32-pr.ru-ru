---
description: 'Дополнительные сведения: структура JET_RECPOS'
title: Структура JET_RECPOS
TOCTitle: JET_RECPOS Structure
ms:assetid: 7c335120-4b84-4095-8f13-e5315d4996b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269308(v=EXCHG.10)
ms:contentKeyID: 32765598
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
ms.openlocfilehash: 8b693f96d80352c758a1700bd2af4e435a948beeb73a268c08e997ef3e3b1d3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107493"
---
# <a name="jet_recpos-structure"></a>Структура JET_RECPOS


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_recpos-structure"></a>Структура JET_RECPOS

Структура **JET_RECPOS** содержит коллекцию целых чисел, представляющих дробную точку в индексе. **центриеслт** — число индексных записей, меньших, чем текущий ключ индекса. **центриесинранже** — количество записей индекса, равное текущему ключу. **центриесинранже** не поддерживается и всегда возвращается как 1. **центриестотал** — количество индексных записей в индексе. Все значения являются приближениями без гарантии точности.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long centriesLT;
      unsigned long centriesInRange;
      unsigned long centriesTotal;
    } JET_RECPOS;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер структуры [JET_RETINFO](./jet-retinfo-structure.md) в байтах. Это значение подтверждает наличие следующих полей.

**центриеслт**

Приблизительное количество элементов индекса меньше текущего.

**центриесинранже**

Приблизительное число записей индекса, равное текущему ключу. Это поле всегда имеет значение 1, независимо от количества записей индекса, фактически равного текущему ключу.

**центриестотал**

Приблизительное количество записей в индексе.

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

[JET_RETINFO](./jet-retinfo-structure.md)  
[жетжетрекордпоситион](./jetgetrecordposition-function.md)
