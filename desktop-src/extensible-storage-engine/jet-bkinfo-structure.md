---
description: 'Дополнительные сведения: структура JET_BKINFO'
title: Структура JET_BKINFO
TOCTitle: JET_BKINFO Structure
ms:assetid: dfaf1d72-1d5f-4777-91c1-6affb735b092
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294120(v=EXCHG.10)
ms:contentKeyID: 32765734
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
ms.openlocfilehash: 6c4849c23e742657d8f5eaba8a030426f7a2a440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272134"
---
# <a name="jet_bkinfo-structure"></a>Структура JET_BKINFO


_**Применимо к:** Windows | Windows Server_

## <a name="jet_bkinfo-structure"></a>Структура JET_BKINFO

Структура **JET_BKINFO** содержит коллекцию данных о конкретном событии резервного копирования.

```cpp
    typedef struct {
      JET_LGPOS lgposMark;
      union {
        JET_LOGTIME logtimeMark;
        JET_BKLOGTIME bklogtimeMark;
      };
      unsigned long genLow;
      unsigned long genHigh;
    } JET_BKINFO;
```

### <a name="members"></a>Элементы

**лгпосмарк**

Идентификатор этой резервной копии.

**логтимемарк**

Время события резервного копирования.

**бклогтимемарк**

Время события резервного копирования с дополнительными битами для указания резервной копии моментального снимка.

**Windows Vista: бклогтимемарк** появился в Windows Vista.

**женлов**

Младший номер создания журнала, связанный с этим событием резервного копирования.

**женхигх**

Старший номер создания журнала, связанный с этим событием резервного копирования.

### <a name="remarks"></a>Комментарии

Эта структура используется в структуре [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) для представления данных о событии резервного копирования базы данных.

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

[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_BKLOGTIME](./jet-bklogtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
