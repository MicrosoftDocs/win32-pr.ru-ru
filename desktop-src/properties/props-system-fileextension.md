---
description: Определяет расширение файла элемента на основе файла, включая начальную точку.
ms.assetid: b72c695e-bdbd-471d-b902-9e30a62facd4
title: System. FileExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf8792a3965c394a1944985515df527e41e3a159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656603"
---
# <a name="systemfileextension"></a>System. FileExtension

Определяет расширение файла элемента на основе файла, включая начальную точку. Это свойство является производным от System. FileName. Если System. имя_файла либо не имеет расширения файла, либо имеет значение VT \_ Empty, значением этого свойства должно быть VT \_ Empty.

Чтобы получить тип любого элемента (включая элемент, который не является файлом), используйте System. ItemType.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.FileExtension
   shellPKey = PKEY_FileExtension
   formatID = E4F10A3C-49E6-405D-8288-A23BD4EEAA6C
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Комментарии

Значения PKEY определены в списке PKEY. h.

Если [System. filename](./props-system-filename.md) является VT \_ пустым, это свойство также должно быть пустым. В противном случае это свойство должно быть получено соответствующим образом источником данных из System. имя_файла. Если System. имя_файла не включает расширение файла, [System. fileExtension]() должно иметь значение VT \_ Empty. Чтобы получить тип любого элемента (включая элемент, который не является файлом), используйте [System. ItemType](./props-system-itemtype.md).

Примеры свойств пути и расширения файла. 

| Путь                               | Расширение файла |
|------------------------------------|----------------|
| c: \\ файлы \\ Personal \\hello.txt     | .txt           |
| \\\\\\Общая папка сервера \\ MyDir \\news.doc | .doc           |
| \\\\\\Общая папка сервера \\numbers.xls     | .xls           |
| \\\\\\Общая \\ папка сервера          | VT \_ пуст      |
| в. \\ \\ MyFolder                | VT \_ пуст      |
| \[desktop\]                        | VT \_ пуст      |



 

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

 

 
