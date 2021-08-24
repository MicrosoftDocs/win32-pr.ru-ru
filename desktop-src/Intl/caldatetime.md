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
ms.openlocfilehash: 700e11f27b673d9ff706483cc4abcf2f06cd7d8bb779ef8eaf9b51a6d81b4068
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822834"
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

**Отображение**
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры поддержки национальных языков](national-language-support-structures.md)
</dt> </dl>

 

 




