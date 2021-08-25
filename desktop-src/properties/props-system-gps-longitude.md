---
description: Указывает долготу.
ms.assetid: ef28141f-1b63-4694-b6df-fcc11ce7e50b
title: System. GPS. Долгота
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12d65c2776c3740360c4cb298048621a877d58999eaddd6e219c682e5a0c9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010344"
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

## <a name="remarks"></a>Remarks

Значения PKEY определены в списке PKEY. h.

`label`для Windows Vista с пакетом обновления 1 (SP1) была добавлена обязательная ссылка на косвенную строку для атрибута **лабелинфо** .

## <a name="related-topics"></a>Связанные темы

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

 

 
