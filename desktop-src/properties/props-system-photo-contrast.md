---
description: Указывает направление обработки контрастности, применяемой камерой при создании образа. &\#0034; 0&\# 0034; указывает &\# 0034; Обычная&\# 0034;; &\# 0034; 1&\# 0034; указывает &\# 0034; Soft&\# 0034;; &\# 0034; 2&\# 0034; указывает &\# 0034; Жесткий&\# 0034;.
ms.assetid: 32f89149-b90d-4fe9-9d1a-b8bb966d62fe
title: System. photo. контраст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4117f13d35a352971a5f9b9f8685816f8ffbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647312"
---
# <a name="systemphotocontrast"></a>System. photo. контраст

Указывает направление обработки контрастности, применяемой камерой при создании образа. "0" означает "нормальный"; "1" означает "Soft"; "2" означает "жесткое".

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Photo.Contrast
   shellPKey = PKEY_Photo_Contrast
   formatID = 2A785BA9-8D23-4DED-82E6-60A350C86A10
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Normal
            value = 0
            text = Normal
            defineToken = PHOTO_CONTRAST_NORMAL
         enum
            name = Soft
            value = 1
            text = Soft
            defineToken = PHOTO_CONTRAST_SOFT
         enum
            name = Hard
            value = 2
            text = Hard
            defineToken = PHOTO_CONTRAST_HARD
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Photo.Contrast
   shellPKey = PKEY_Photo_Contrast
   formatID = 2A785BA9-8D23-4DED-82E6-60A350C86A10
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Normal
            defineName = PHOTO_CONTRAST_NORMAL
         enum
            value = 1
            text = Soft
            defineName = PHOTO_CONTRAST_SOFT
         enum
            value = 2
            text = Hard
            defineName = PHOTO_CONTRAST_HARD
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

 

 
