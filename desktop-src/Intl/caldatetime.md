---
description: Не рекомендуется. Представляет мгновенное время, обычно выраженное как Дата и время суток, и соответствующий календарь.
ms.assetid: a714ff32-2b1f-4256-931e-324d64daf2ac
title: Структура КАЛДАТЕТИМЕ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e3f0099a8e1dd7794b960af3d753085f2a32eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684681"
---
# <a name="caldatetime-structure"></a>Структура КАЛДАТЕТИМЕ

Не рекомендуется. Представляет мгновенное время, обычно выраженное как Дата и время суток, и соответствующий календарь.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _caldatetime {
  CALID CalId;
  UINT  Era;
  UINT  Year;
  UINT  Month;
  UINT  Day;
  UINT  DayOfWeek;
  UINT  Hour;
  UINT  Minute;
  UINT  Second;
  ULONG Tick;
} CALDATETIME, *LPCALDATETIME;
```



## <a name="members"></a>Члены

<dl> <dt>

**калид**
</dt> <dd>

[Идентификатор календаря](calendar-identifiers.md) для мгновенного выполнения.

</dd> <dt>

**Нашей**
</dt> <dd>

Сведения о эре за текущий момент времени.

</dd> <dt>

**Год**
</dt> <dd>

Год на момент времени.

</dd> <dt>

**Месяц**
</dt> <dd>

Месяц на момент времени.

</dd> <dt>

**День**
</dt> <dd>

День на момент времени.

</dd> <dt>

**DayOfWeek**
</dt> <dd>

День недели для мгновенного выполнения.

</dd> <dt>

**Час**
</dt> <dd>

Час на момент времени.

</dd> <dt>

**Интервал**
</dt> <dd>

Минута на момент времени.

</dd> <dt>

**Секунды**
</dt> <dd>

Второй для мгновенного выполнения.

</dd> <dt>

**Импульс**
</dt> <dd>

Такт на момент времени.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры поддержки национальных языков](national-language-support-structures.md)
</dt> </dl>

 

 




