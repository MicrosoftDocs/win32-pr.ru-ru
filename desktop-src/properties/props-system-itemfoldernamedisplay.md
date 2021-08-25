---
description: Понятное пользователю отображаемое имя родительской папки элемента.
ms.assetid: 4049b6cb-41a1-4df6-89d1-a2022d3a285d
title: System. Итемфолдернамедисплай
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c8e8ca12af7c7665a2fd4b64f2911a1e6dbc99805cf4355ea1bb1ceec764c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119945174"
---
# <a name="systemitemfoldernamedisplay"></a>System. Итемфолдернамедисплай

Понятное пользователю отображаемое имя родительской папки элемента.

Это является производным от [System. итемфолдерпасдисплай](./props-system-itemfolderpathdisplay.md). Если это свойство имеет значение VT \_ Empty, это свойство также должно быть.

Если папка является папкой файлов, значение будет локализовано, если локализованное имя доступно.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemFolderNameDisplay
   shellPKey = PKEY_ItemFolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Remarks

Значения PKEY определены в списке PKEY. h.

Если [System. итемфолдерпасдисплай](./props-system-itemfolderpathdisplay.md) является VT \_ пустым, это свойство также должно быть пустым. В противном случае он должен быть получен соответствующим образом источником данных из System. Итемфолдерпасдисплай.

Примеры:



| Заданный путь                             | Отображаемое имя папки |
|----------------------------------------|---------------------|
| c: \\ мифилес \\ Text \\hello.txt           | Текст                |
| \\\\\\Общая папка сервера \\ MyDir \\goodnews.doc | MyDir               |
| \\\\\\Общая папка сервера \\numbers.xls         | поделиться               |
| c: \\ папки \\ MyFolder                  | Папки             |
| Учетная запись/маилбокс/Inbox/"Re: Hello!"    | Папка "Входящие"               |



 

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

 

 
