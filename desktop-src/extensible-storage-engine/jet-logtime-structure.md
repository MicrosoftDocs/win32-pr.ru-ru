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
ms.openlocfilehash: 9cb6fac65451518e20dd64ee223638165ac5c752
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470479"
---
# <a name="jet_logtime-structure"></a>Структура JET_LOGTIME


_**Применимо к:** Windows | Windows Сервером_

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


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
