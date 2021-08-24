---
description: Прочитайте о свойстве System. Итемфолдерпасдисплай, которое представляет понятный пользователю отображаемый путь к родительской папке элемента.
ms.assetid: 16f67edc-ca8a-4c2e-9d9b-be8600446e51
title: System. Итемфолдерпасдисплай
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fd2288f12073fe8e36707bf49aca2bc5e000d0bbe25d95fba0736b4e77af44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822344"
---
# <a name="systemitemfolderpathdisplay"></a>System. Итемфолдерпасдисплай

Понятный пользователю отображаемый путь к родительской папке элемента.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemFolderPathDisplay
   shellPKey = PKEY_ItemFolderPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 6
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Remarks

Значения PKEY определены в списке PKEY. h.

Если [System. итемпасдисплай](./props-system-itempathdisplay.md) является VT \_ пустым, это свойство также должно быть пустым. В противном случае он должен быть получен соответствующим образом источником данных из System. Итемпасдисплай.

Примеры значений



| Путь                                   | итемфолдерпасдисплай    |
|----------------------------------------|--------------------------|
| c: \\ файлы \\ Personal \\hello.txt         | c: \\ файлы \\ личные      |
| \\\\\\Общая папка сервера \\ MyDir \\goodnews.doc | \\\\\\Общая папка сервера \\ MyDir |
| \\\\\\Общая папка сервера \\numbers.xls         | \\\\\\Общая папка сервера        |
| в. \\ еда \\ MyFolder                     | c: \\ еда                 |
| Учетная запись/маилбокс/Inbox/"Re: Hello!"    | Учетная запись/маилбокс/входящие   |



 

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

 

 
