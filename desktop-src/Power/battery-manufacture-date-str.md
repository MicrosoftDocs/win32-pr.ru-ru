---
description: Содержит дату изготовления аккумулятора.
ms.assetid: 0cda66fc-bf4a-4a38-b43c-6eecde46c414
title: Структура BATTERY_MANUFACTURE_DATE (Покласс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_MANUFACTURE_DATE
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: cdd3f067bc3ed2e3339710e0a5bd48c8f42e6525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663129"
---
# <a name="battery_manufacture_date-structure"></a>\_ \_ Структура даты изготовления аккумулятора

Содержит дату изготовления аккумулятора. Эта структура используется структурой [**\_ \_ сведений о заряде аккумулятора**](battery-query-information-str.md) при запросе уровня информации баттеримануфактуредате.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _BATTERY_MANUFACTURE_DATE {
  UCHAR  Day;
  UCHAR  Month;
  USHORT Year;
} BATTERY_MANUFACTURE_DATE, *PBATTERY_MANUFACTURE_DATE;
```



## <a name="members"></a>Члены

<dl> <dt>

**День**
</dt> <dd>

День изготовления месяца в диапазоне от 1 до 31. Несмотря на тип данных, это значение не кодируется в кодировке ASCII. Это байт без знака.

</dd> <dt>

**Месяц**
</dt> <dd>

Месяц изготовления в диапазоне от 1 (январь) до 12 (декабрь). Несмотря на тип данных, это значение не кодируется в кодировке ASCII. Это байт без знака.

</dd> <dt>

**Год**
</dt> <dd>

Год изготовления. Обычно они находятся в диапазоне 1900-2100.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Дата кодируется в григорианском или Западной календарном формате.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                                                                                                                                                                                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Покласс. h; </dt> <dt>Баткласс. h в Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ сведения о запросе аккумулятора**](battery-query-information-str.md)
</dt> <dt>

[**\_ \_ сведения о запросе от аккумулятора ioctl \_**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




