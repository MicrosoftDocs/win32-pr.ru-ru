---
description: При использовании параметра CONTAINS в индексе поиска Windows это число совпадений термина. Если имеется несколько элементов CONTAINS,, то при этом вычисляются минимальное число попаданий, а или — максимальное число попаданий.
ms.assetid: 2f0cddba-7535-451f-9bb5-846c06c426f8
title: System. Search. Хиткаунт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bb3954d891c1f7c913036449094c27f64cea7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719698"
---
# <a name="systemsearchhitcount"></a>System. Search. Хиткаунт

При использовании параметра CONTAINS в индексе поиска Windows это число совпадений термина. Если имеется несколько элементов CONTAINS,, то при этом вычисляются минимальное число попаданий, а или — максимальное число попаданий.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.HitCount
   shellPKey = PKEY_Search_HitCount
   formatID = 49691C90-7E17-101A-A91C-08002B2ECDA9
   propID = 4
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Int32
      IsInnate = true
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

 

 
