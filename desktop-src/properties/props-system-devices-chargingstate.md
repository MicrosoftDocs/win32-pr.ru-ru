---
description: Состояние зарядки устройства.
ms.assetid: 33ef8ecb-29e3-4809-9d56-8d884f9c9ff6
title: System. Devices. Чаргингстате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de306cc44900849d74ba24924c9c4066c0ffe0a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081461"
---
# <a name="systemdeviceschargingstate"></a>System. Devices. Чаргингстате

Состояние зарядки устройства.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Devices.ChargingState
   shellPKey = PKEY_Devices_ChargingState
   formatID = 49CD1F76-5626-4B17-A4E8-18B4AA1A2213
   propID = 11
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Byte
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = NotCharging
            minValue = 0
            setValue = 0
            text = Not charging
            defineToken = CHARGINGSTATE_NOT_CHARGING
         enumRange
            name = Charging
            minValue = 1
            setValue = 1
            text = Charging
            defineToken = CHARGINGSTATE_CHARGING
         enumRange
            name = UnknownChargingState
            minValue = 2
            setValue = 2
            text = Unknown charging state
            defineToken = CHARGINGSTATE_UNKNOWN_STATE
```

## <a name="remarks"></a>Комментарии

Значения PKEY определены в списке PKEY. h.

## <a name="related-topics"></a>См. также

<dl> <dt>

[пропертидескриптион](./propdesc-schema-propertydescription.md)
</dt> <dt>

[сеарчинфо](./propdesc-schema-searchinfo.md)
</dt> <dt>

[лабелинфо](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[булеанформат](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[енумератедлист](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[дравконтрол](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[едитконтрол](./propdesc-schema-editcontrol.md)
</dt> <dt>

[филтерконтрол](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[куериконтрол](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
