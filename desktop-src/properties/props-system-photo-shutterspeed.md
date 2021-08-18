---
description: Скорость затвора камеры, когда была сделана фотография. Это указывается в единицах ВЕРШИНЕ.
ms.assetid: 7f51b3b9-d701-4e7a-80bd-87c1a60e56f7
title: System. photo. Шуттерспид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b14e5a919019e7e1f48bc8a65105c649f51745f1d33cda8518a0bfa501155ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970053"
---
# <a name="systemphotoshutterspeed"></a>System. photo. Шуттерспид

Скорость затвора камеры, когда была сделана фотография. Это указывается в единицах ВЕРШИНЕ. Это свойство вычисляется из [System. photo. шуттерспиднумератор](./props-system-photo-shutterspeednumerator.md) и [System. photo. шуттерспидденоминатор](./props-system-photo-shutterspeeddenominator.md).

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Photo.ShutterSpeed
   shellPKey = PKEY_Photo_ShutterSpeed
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37377
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Photo.ShutterSpeed
   shellPKey = PKEY_Photo_ShutterSpeed
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37377
   SearchInfo
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a>Remarks

Значения PKEY определены в списке PKEY. h.

Чтобы преобразовать это значение в время выдержки, см. спецификацию файла обмена изображениями (EXIF) 2,2 в приложении C. Используйте [System. photo. експосуретиме](./props-system-photo-exposuretime.md) в любых представлениях оболочки вместо [System. photo. шуттерспид]().

## <a name="related-topics"></a>Связанные темы

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

 

 
