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
ms.openlocfilehash: ed374030bd3ab577b209d326d21110482c9cf37a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989117"
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


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_RETINFO](./jet-retinfo-structure.md)  
[жетжетрекордпоситион](./jetgetrecordposition-function.md)
