---
description: Имя файла, включая его расширение.
ms.assetid: 40940026-6c67-4196-aff6-5f846dc94f27
title: System. имя_файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8a92febe0a4f2dfe8cc9d5741118fdb76bcb56c7bcd1ef5c3d881e8c0f9abf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119096923"
---
# <a name="systemfilename"></a>System. имя_файла

Имя файла, включая его расширение. System. FileExtension является производным от этого свойства.

Возможно, элемент не существует в файловой системе (то есть он может быть не открыт с помощью CreateFile). Тем не менее, если элемент представлен в виде файла, а его имя соответствует стандартному синтаксису именования файлов Win32, то источник данных должен выдать это свойство. Если элемент не является файлом, источник данных должен порождать это свойство как VT \_ Empty.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = 0-9
         enumRange
            minValue = A
            setValue = A
            text = A-H
         enumRange
            minValue = I
            setValue = I
            text = I-P
         enumRange
            minValue = Q
            setValue = Q
            text = Q-Z
```

## <a name="remarks"></a>Remarks

Значения PKEY определены в списке PKEY. h.

Элемент может не существовать в файловой системе (то есть он может быть не открыт с помощью CreateFile), но если элемент представлен в виде файла из логического датчика, а его имя соответствует стандартному синтаксису именования файлов Win32, то источник данных должен выдать это свойство. Если элемент не является файлом, значение этого свойства — VT \_ Empty. См. раздел System. Итемнамедисплай. Оно имеет то же значение, что и System. Парсингнаме для элементов, которые предоставляются в папке файлов оболочки.

В следующей таблице приведены примеры значений свойств Path и filename.



| Путь                               | Значение свойства |
|------------------------------------|----------------|
| c: \\ файлы \\ Personal \\hello.txt     | hello.txt      |
| \\\\\\Общая папка сервера \\ MyDir \\news.doc | news.doc       |
| \\\\\\Общая папка сервера \\numbers.xls     | numbers.xls    |
| в. \\ \\ MyFolder                | MyFolder       |
| \[сообщение электронной почты\]                  | VT \_ пуст      |
| \[песня. WMA на портативном устройстве\]    | песня. WMA       |



 

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

 

 
