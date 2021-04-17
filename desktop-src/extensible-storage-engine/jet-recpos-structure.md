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
ms.openlocfilehash: e24e16aaac4228f35350f55f57a14f2820add0cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712421"
---
# <a name="jet_recpos-structure"></a>Структура JET_RECPOS


_**Применимо к:** Windows | Windows Server_

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

[JET_RETINFO](./jet-retinfo-structure.md)  
[жетжетрекордпоситион](./jetgetrecordposition-function.md)
