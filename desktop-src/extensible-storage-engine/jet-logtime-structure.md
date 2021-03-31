---
description: 'Дополнительные сведения: структура JET_LOGTIME'
title: Структура JET_LOGTIME
TOCTitle: JET_LOGTIME Structure
ms:assetid: cb7c0b74-db7a-4e48-80b8-37b3fdf6d088
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294089(v=EXCHG.10)
ms:contentKeyID: 32765704
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
ms.openlocfilehash: 9c99e2c1f77a01c33a75d3e5d16c4fe58c122a4e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "103821589"
---
# <a name="jet_logtime-structure"></a>Структура JET_LOGTIME


_**Применимо к:** Windows | Windows Server_

## <a name="jet_logtime-structure"></a>Структура JET_LOGTIME

Структура **JET_LOGTIME** содержит элементы даты и времени события.

```cpp
typedef struct {
  char bSeconds;
  char bMinutes;
  char bHours;
  char bDay;
  char bMonth;
  char bYear;
  union {
    char bFiller1;
    struct {
        unsigned char fTimeIsUTC: 1;
        unsigned char fUnused: 7;
    };
  };
  char bFiller2;
} JET_LOGTIME;
```

### <a name="members"></a>Элементы

**бсекондс**

Время события в секундах. Это значение может быть от 0 до 59. 0 используется, если структура имеет значение null.

**бминутес**

Время события в минутах. Это значение может быть от 0 до 59. 0 используется, если структура имеет значение null.

**бхаурс**

Время события в часах. Это значение может быть от 0 до 23. 0 используется, если структура имеет значение null.

**бдай**

День месяца события. Это значение может быть от 0 до 31. 0 используется, если структура имеет значение null.

**бмонс**

Месяц года события. Это значение может быть от 0 до 12. 0 используется, если структура имеет значение null.

**беар**

Год события (смещение на 1900). Чтобы достичь фактического года, добавьте 1900 к этому значению. 0 используется, если структура имеет значение null.

**bFiller1**

Это поле следует игнорировать.

**фтимеисутк**

Время указано в формате UTC.

**фунусед**

Это поле следует игнорировать.

**bFiller2**

Это поле следует игнорировать.

### <a name="remarks"></a>Комментарии

Эта структура предназначена главным образом для использования при отладке.

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

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
