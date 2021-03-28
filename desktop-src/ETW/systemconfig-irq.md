---
description: Этот класс является классом типа событий для событий запросов на прерывание (IRQ). Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 9d4692e8-f19f-478c-a003-396722e426c3
title: Класс SystemConfig_IRQ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IRQ
- SystemConfig_IRQ.IRQAffinity
- SystemConfig_IRQ.IRQNum
- SystemConfig_IRQ.DeviceDescriptionLen
- SystemConfig_IRQ.DeviceDescription
api_type:
- NA
api_location: ''
ms.openlocfilehash: e1dd674c34c06259bc343615c17d165be3f57d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984456"
---
# <a name="systemconfig_irq-class"></a>\_Класс системконфиг IRQ

Этот класс является классом типа событий для событий запросов на прерывание (IRQ).

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(21), EventTypeName("IRQ")]
class SystemConfig_IRQ : SystemConfig
{
  uint64 IRQAffinity;
  uint32 IRQNum;
  uint32 DeviceDescriptionLen;
  string DeviceDescription;
};
```

## <a name="members"></a>Участники

Класс **системконфиг \_ IRQ** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **системконфиг \_ IRQ** имеет эти свойства.

<dl> <dt>

**DeviceDescription**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4), Стрингтерминатион ("NullTerminated"), Format ("w")
</dt> </dl>

Описание устройства или программного обеспечения, выполняющего запрос.

</dd> <dt>

**девицедескриптионлен**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3)
</dt> </dl>

Длина строки в **DeviceDescription** в символах.

</dd> <dt>

**иркаффинити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1), Format ("x")
</dt> </dl>

Маска сходства IRQ. Маска сходства определяет конкретные процессоры (или группы процессоров), которые могут получить IRQ.

</dd> <dt>

**иркнум**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2)
</dt> </dl>

Номер строки запроса на прерывание.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**системконфиг**](systemconfig.md)
</dt> </dl>

 

 




