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
ms.openlocfilehash: 2b84de9a4f64db5dda261b8ee177787f62fd01ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702800"
---
# <a name="jet_threadstats-structure"></a>Структура JET_THREADSTATS


_**Применимо к:** Windows | Windows Server_

## <a name="jet_threadstats-structure"></a>Структура JET_THREADSTATS

Структура **JET_THREADSTATS** содержит совокупную статистику по работе, выполненной ядром СУБД в текущем потоке. Эти сведения возвращаются через [жетжетсреадстатс](./jetgetthreadstats-function.md).

**Windows Vista:**  Структура **JET_THREADSTATS** появилась в Windows Vista.

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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также:

[жетжетсреадстатс](./jetgetthreadstats-function.md)
