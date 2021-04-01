---
description: Указывает долготу.
ms.assetid: ef28141f-1b63-4694-b6df-fcc11ce7e50b
title: System. GPS. Долгота
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e65431412b0d46ad7b68100febd4d6e8efd31a17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156895"
---
# <a name="systemgpslongitude"></a>System. GPS. Долгота

Указывает долготу. Это массив из трех значений, как показано ниже: индекс 0 — это градусы, индекс 1 — минуты, индекс 2 — секунды. Каждый из них вычисляется на основе значений в списке PKEY \_ GPS \_ ЛОНГИТУДЕНУМЕРАТОР и PKEY \_ GPS \_ лонгитудеденоминатор.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8

```
propertyDescription
   name = System.GPS.Longitude
   shellPKey = PKEY_GPS_Longitude
   formatID = C4C4DBB2-B593-466B-BBDA-D03D27D5E43A
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="windows-7-windows-vista"></a>Windows 7, Windows Vista

```
propertyDescription
   name = System.GPS.Longitude
   shellPKey = PKEY_GPS_Longitude
   formatID = C4C4DBB2-B593-466B-BBDA-D03D27D5E43A
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="remarks"></a>Комментарии

Значения PKEY определены в списке PKEY. h.

`label`Для Windows Vista с пакетом обновления 1 (SP1) был добавлен запрос на указанную косвенную ссылку на непрямое строковое значение атрибута **лабелинфо** .

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

 

 
