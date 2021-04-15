---
description: Определяет, зашифрован ли элемент.
ms.assetid: fd93f915-6af3-4bde-982e-6774a1ca83af
title: System. с шифрованием
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05f6f1d31838f885820938e9be38ef161c168ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647317"
---
# <a name="systemisencrypted"></a>System. с шифрованием

Определяет, зашифрован ли элемент.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.IsEncrypted
   shellPKey = PKEY_IsEncrypted
   formatID = 90E5E14E-648B-4826-B2AA-ACAF790E3513
   propID = 10
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Boolean
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Encrypted
            value = #TRUE#
            text = Encrypted
            defineToken = ISENCRYPTED_ENCRYPTED
         enum
            name = NotEncrypted
            value = #FALSE#
            text = Unencrypted
            defineToken = ISENCRYPTED_NOTENCRYPTED
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.IsEncrypted
   shellPKey = PKEY_IsEncrypted
   formatID = 90E5E14E-648B-4826-B2AA-ACAF790E3513
   propID = 10
   SearchInfo
      IsColumn = true
   typeInfo
      type = Boolean
      EnumeratedList
         UseValueForDefault = True
         enum
            value = #TRUE#
            text = Encrypted
            mnemonics = encrypted
         enum
            value = #FALSE#
            text = Unencrypted
            mnemonics = unencrypted
```

## <a name="remarks"></a>Комментарии

Значения PKEY определены в списке PKEY. h.

Это свойство было введено в выпуске Windows Search 4,0.

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

 

 
