---
description: Система оценок, использующая диапазон целочисленных значений от 0 до 5.
ms.assetid: 50353ba9-86dd-4172-91b4-1898c8fc5522
title: System. Симплератинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e13d7f65fb335aea6362509c20845bd1324b6e99d48f14cd9746f0237661f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119598144"
---
# <a name="systemsimplerating"></a>System. Симплератинг

Система оценок, использующая диапазон целочисленных значений от 0 до 5.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.SimpleRating
   shellPKey = PKEY_SimpleRating
   formatID = A09F084E-AD41-489F-8076-AA5BE3082BCA
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="remarks"></a>Remarks

Значения PKEY определены в списке PKEY. h.

для обеспечения совместимости с системой оценки оболочки Windows Vista обработчик свойств также должен заполнить свойство [system. рейтингов](./props-system-rating.md) с сопоставлением, как описано для этого свойства.

Используйте следующую таблицу для преобразования из [System. рейтингов](./props-system-rating.md) в [System. симплератинг]().



| System. Оценка | System. Симплератинг |
|---------------|---------------------|
| 0             | 0                   |
| 1–12          | 1                   |
| 13-37         | 2                   |
| 38-62         | 3                   |
| 63-87         | 4                   |
| 88-99         | 5                   |



 

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

 

 
