---
description: Не рекомендуется. Указывает единицы даты для настройки структуры КАЛДАТЕТИМЕ.
ms.assetid: 20d0cd7a-6e6b-4c82-9cfa-e4f4315d6362
title: Перечисление CALDATETIME_DATEUNIT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME_DATEUNIT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6ce1f8929dd6e2f7de59d32d66229f73c062505c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682634"
---
# <a name="caldatetime_dateunit-enumeration"></a>\_Перечисление ДАТЕУНИТ калдатетиме

Не рекомендуется. Указывает единицы даты для настройки структуры [**калдатетиме**](caldatetime.md) .

## <a name="syntax"></a>Синтаксис


```C++
enum CALDATETIME_DATEUNIT {
  EraUnit, 
  YearUnit, 
  MonthUnit, 
  WeekUnit, 
  DayUnit, 
  HourUnit, 
  MinuteUnit, 
  SecondUnit, 
  TickUnit 

};
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="EraUnit"></span><span id="eraunit"></span><span id="ERAUNIT"></span>**ераунит**
</dt> <dd>

Единица времени эры даты.

</dd> <dt>

<span id="YearUnit"></span><span id="yearunit"></span><span id="YEARUNIT"></span>**еарунит**
</dt> <dd>

Единица измерения даты и времени года.

</dd> <dt>

<span id="MonthUnit"></span><span id="monthunit"></span><span id="MONTHUNIT"></span>**монсунит**
</dt> <dd>

Единица времени месяца даты.

</dd> <dt>

<span id="WeekUnit"></span><span id="weekunit"></span><span id="WEEKUNIT"></span>**викунит**
</dt> <dd>

Единица времени для даты недели.

</dd> <dt>

<span id="DayUnit"></span><span id="dayunit"></span><span id="DAYUNIT"></span>**дайунит**
</dt> <dd>

Единица времени дня и даты.

</dd> <dt>

<span id="HourUnit"></span><span id="hourunit"></span><span id="HOURUNIT"></span>**хаурунит**
</dt> <dd>

Единица времени часового периода.

</dd> <dt>

<span id="MinuteUnit"></span><span id="minuteunit"></span><span id="MINUTEUNIT"></span>**минутеунит**
</dt> <dd>

Единица времени в виде минуты.

</dd> <dt>

<span id="SecondUnit"></span><span id="secondunit"></span><span id="SECONDUNIT"></span>**секондунит**
</dt> <dd>

Вторая единица времени даты.

</dd> <dt>

<span id="TickUnit"></span><span id="tickunit"></span><span id="TICKUNIT"></span>**тиккунит**
</dt> <dd>

Единица времени даты Tick.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Типы перечисления поддержки национальных языков](national-language-support-enumeration-types.md)
</dt> </dl>

 

 




