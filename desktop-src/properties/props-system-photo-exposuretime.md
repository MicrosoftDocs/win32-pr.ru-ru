---
description: Время раскрытия фотографии (в секундах), считанное из данных файла изображения (EXIF).
ms.assetid: 44f7e6d5-c4d9-4b41-b6c6-15145abb7983
title: System. photo. Експосуретиме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5811a3d375f41883d1db8f392e714b7bbe0dfa8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264235"
---
# <a name="systemphotoexposuretime"></a>System. photo. Експосуретиме

Время раскрытия фотографии (в секундах), считанное из данных файла изображения (EXIF). Это свойство вычисляется из [System. photo. експосуретименумератор](./props-system-photo-exposuretimenumerator.md) и [System. photo. експосуретимеденоминатор](./props-system-photo-exposuretimedenominator.md).

Ниже приведен список возможных значений, взятых из спецификации EXIF 2,2.

-   30
-   15
-   8
-   4
-   2
-   1
-   1/2
-   1/4
-   1/8
-   1/15
-   1/30
-   1/60
-   1/125
-   1/250
-   1/500
-   1/1000
-   1/2000

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Photo.ExposureTime
   shellPKey = PKEY_Photo_ExposureTime
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 33434
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a>Комментарии

Значения PKEY определены в списке PKEY. h.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Формат файла изображения для обмена по-прежнему для цифровых камер: EXIF версии 2,2](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

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

 

 
