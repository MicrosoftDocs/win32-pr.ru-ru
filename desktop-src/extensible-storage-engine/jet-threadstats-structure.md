---
description: 'Дополнительные сведения: структура JET_THREADSTATS'
title: Структура JET_THREADSTATS
TOCTitle: JET_THREADSTATS Structure
ms:assetid: 37e86e14-7719-4991-aae8-bcff1baa80df
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269227(v=EXCHG.10)
ms:contentKeyID: 32765529
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
ms.openlocfilehash: 7f94c9911fb7ab974f87cfed41e92b53ac0a66cb
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983567"
---
# <a name="jet_threadstats-structure"></a>Структура JET_THREADSTATS


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_threadstats-structure"></a>Структура JET_THREADSTATS

Структура **JET_THREADSTATS** содержит совокупную статистику по работе, выполненной ядром СУБД в текущем потоке. Эти сведения возвращаются через [жетжетсреадстатс](./jetgetthreadstats-function.md).

**Windows Vista:**  структура **JET_THREADSTATS** появилась в Windows Vista.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cPageReferenced;
      unsigned long cPageRead;
      unsigned long cPagePreread;
      unsigned long cPageDirtied;
      unsigned long cPageRedirtied;
      unsigned long cLogRecord;
      unsigned long cbLogRecord;
    } JET_THREADSTATS;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер возвращаемой структуры **JET_THREADSTATS** в байтах.

**Примечание**  .  Структура **JET_THREADSTATS** будет расширена в будущем, чтобы она содержала больше статистики. Новая статистика будет добавлена в конец структуры и может быть извлечена с увеличением размера выходного буфера. Наличие дополнительной статистики может быть выведено с помощью большего значения **кбструкт** .

**кпажереференцед**

Общее число страниц базы данных, посещенных ядром СУБД в текущем потоке.

**кпажереад**

Общее число страниц базы данных, извлекаемых с диска ядром СУБД в текущем потоке.

**кпажепререад**

Общее число страниц базы данных, выбранных с диска ядром СУБД в текущем потоке.

**кпажедиртиед**

Общее число страниц базы данных без незаписанных изменений, которые были изменены ядром СУБД в текущем потоке.

**кпажередиртиед**

Общее число страниц базы данных с незаписанными изменениями, которые были изменены ядром СУБД в текущем потоке.

**клогрекорд**

Общее число записей журнала транзакций, созданных ядром СУБД в текущем потоке.

**кблогрекорд**

Общий размер в байтах записей журнала транзакций, созданных ядром СУБД в текущем потоке.

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[жетжетсреадстатс](./jetgetthreadstats-function.md)
