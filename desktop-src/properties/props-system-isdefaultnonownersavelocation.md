---
description: Определяет место сохранения библиотеки по умолчанию для владельцев библиотеки, не являющихся владельцами.
ms.assetid: e6fe96de-4895-477e-a442-746fd34a7433
title: System. Исдефаултноновнерсавелокатион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c0922ab8667784ad4ab0394767786c9ecc555c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711263"
---
# <a name="systemisdefaultnonownersavelocation"></a>System. Исдефаултноновнерсавелокатион

Определяет место сохранения библиотеки по умолчанию для владельцев библиотеки, не являющихся владельцами.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8

```
propertyDescription
   name = System.IsDefaultNonOwnerSaveLocation
   shellPKey = PKEY_IsDefaultNonOwnerSaveLocation
   formatID = 5D76B67F-9B3D-44BB-B6AE-25DA4F638A67
   propID = 5
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      EnumeratedList
         UseValueForDefault = True
         enum
            name = DefaultPublicSave
            value = #TRUE#
            text = Public save location
            defineToken = ISDEFAULTPUBLICSAVE_YES
         enum
            name = NotDefaultPublicSave
            value = #FALSE#
            text
            defineToken = ISDEFAULTPUBLICSAVE_NO
```

## <a name="windows-7"></a>Windows 7

```
propertyDescription
   name = System.IsDefaultNonOwnerSaveLocation
   shellPKey = PKEY_IsDefaultNonOwnerSaveLocation
   formatID = 5D76B67F-9B3D-44BB-B6AE-25DA4F638A67
   propID = 5
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
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

 

 
