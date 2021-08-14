---
description: 'Дополнительные сведения: структура JET_BKLOGTIME'
title: Структура JET_BKLOGTIME
TOCTitle: JET_BKLOGTIME Structure
ms:assetid: 31460079-7c5b-4145-837d-b112ba0117d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269219(v=EXCHG.10)
ms:contentKeyID: 32765522
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
ms.openlocfilehash: b34740d582e341cce3b2fd0b28203b7346a4de1d94a8586289be8ab252247943
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118487726"
---
# <a name="jet_bklogtime-structure"></a>Структура JET_BKLOGTIME


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_bklogtime-structure"></a>Структура JET_BKLOGTIME

Структура **JET_BKLOGTIME** содержит элементы даты и времени события. Это расширение [JET_LOGTIME](./jet-logtime-structure.md).

**Windows vista: JET_BKLOGTIME** введены в Windows vista.

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
      union {
        char bFiller2;
        struct {
          unsigned char fOSSnapshot  :1;
          unsigned char fReserved  :7;
        };
      };
    } JET_BKLOGTIME;
```

### <a name="members"></a>Элементы

**бсекондс**

Время события в секундах. Это может быть 0 (ноль) до 60. 0 (нуль) используется, если структура **JET_BKLOGTIME** имеет значение null.

**бминутес**

Время события в минутах. Это может быть 0 (ноль) до 60. 0 (нуль) используется, если структура **JET_BKLOGTIME** имеет значение null.

**бхаурс**

Время события в часах. Может иметь значение от 0 до 24. 0 (нуль) используется, если структура **JET_BKLOGTIME** имеет значение null.

**бдай**

День месяца события. Может иметь значение от 0 до 31. 0 (нуль) используется, если структура **JET_BKLOGTIME** имеет значение null.

**бмонс**

Месяц года события. Это может быть 0 (нуля) до 12. 0 (нуль) используется, если структура **JET_BKLOGTIME** имеет значение null.

**беар**

Год (смещение на 1900) события. Чтобы достичь фактического года, добавьте 1900 к этому значению. 0 (нуль) используется, если структура **JET_BKLOGTIME** имеет значение null.

**bFiller1**

Это поле следует игнорировать.

**фтимеисутк**

Время указано в формате UTC.

**фунусед**

Это поле следует игнорировать.

**bFiller2**

Это поле следует игнорировать.

**фосснапшот**

Если это событие является резервной копией, этот флаг содержит одно из следующих возможных значений:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Потоковая Архивация</p></td>
<td><p>0 (ноль)</p></td>
</tr>
<tr class="even">
<td><p>Резервное копирование моментальных снимков</p></td>
<td><p>1</p></td>
</tr>
</tbody>
</table>


**фресервед**

Это поле следует игнорировать.

### <a name="remarks"></a>Remarks

Эта структура используется при отладке.

### <a name="requirements"></a>Requirements (Требования)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>требуется Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Сервер</strong></p></td>
<td><p>требуется Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также

[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
