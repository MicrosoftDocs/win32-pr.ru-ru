---
description: Этот класс является классом типа событий для событий канала IDE. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 2265a4a6-4377-4aa9-926a-def6e8eda998
title: Класс SystemConfig_IDEChannel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IDEChannel
- SystemConfig_IDEChannel.TargetId
- SystemConfig_IDEChannel.DeviceType
- SystemConfig_IDEChannel.DeviceTimingMode
- SystemConfig_IDEChannel.LocationInformationLen
- SystemConfig_IDEChannel.LocationInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60cdfcec8f62e6fb96dcedc895d874f01a209430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541866"
---
# <a name="systemconfig_idechannel-class"></a>\_Класс системконфиг идечаннел

Этот класс является классом типа событий для событий канала IDE.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(23), EventTypeName("IDEChannel")]
class SystemConfig_IDEChannel : SystemConfig
{
  uint32 TargetId;
  uint32 DeviceType;
  uint32 DeviceTimingMode;
  uint32 LocationInformationLen;
  string LocationInformation;
};
```

## <a name="members"></a>Участники

Класс **системконфиг \_ идечаннел** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **системконфиг \_ идечаннел** имеет следующие свойства.

<dl> <dt>

**девицетимингмоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3), Format ("x")
</dt> </dl>

Режим, в котором может работать интегрированная среда разработки. Допустимы следующие значения:

-   PIO \_ MODE0 (0x1)
-   PIO \_ MODE1 (0x2)
-   \_MODE2 Pio (0x4)
-   PIO \_ MODE3 (0x8)
-   PIO \_ MODE4 (0x10)
-   СВДМА \_ MODE0 (0x20)
-   СВДМА \_ MODE1 (0x40)
-   СВДМА \_ MODE2 (0x80)
-   МВДМА \_ MODE0 (0x100)
-   МВДМА \_ MODE2 (0x200)
-   МВДМА \_ MODE3 (0x400)
-   UDMA \_ MODE0 (0x800)
-   UDMA \_ MODE1 (0x1000)
-   UDMA \_ MODE2 (0x2000)
-   UDMA \_ MODE3 (0x4000)
-   UDMA \_ MODE4 (0x8000)
-   UDMA \_ MODE5 (0x10000)

</dd> <dt>

**DeviceType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2), Format ("x")
</dt> </dl>

Тип устройства. Допустимы следующие значения:

-   ATA (1)
-   ATAPI (2)

</dd> <dt>

**локатионинформатион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (5), Стрингтерминатион ("NullTerminated"), Format ("w")
</dt> </dl>

Канал IDE (например, основной канал, дополнительный канал и т. д.).

</dd> <dt>

**локатионинформатионлен**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4)
</dt> </dl>

Длина строки **локатионинформатион** .

</dd> <dt>

**TargetId**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1)
</dt> </dl>

Идентификатор диска.

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

 

 




