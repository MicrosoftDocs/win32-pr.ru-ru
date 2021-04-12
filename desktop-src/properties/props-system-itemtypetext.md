---
description: Понятное пользователю имя типа элемента.
ms.assetid: 5d4c86da-6317-4a34-88d6-caf794aaa165
title: System. Итемтипетекст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699a953392054cb2344c5f3b3d652e64a9a2c1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264258"
---
# <a name="systemitemtypetext"></a>System. Итемтипетекст

Понятное пользователю имя типа элемента. Это значение не предназначено для программного синтаксического анализа.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemTypeText
   shellPKey = PKEY_ItemTypeText
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 4
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Комментарии

Значения PKEY определены в списке PKEY. h.

Если [System. ItemType](./props-system-itemtype.md) является VT \_ пустым, значение этого свойства также является VT \_ пустым. Если элемент является файлом, значение этого свойства будет таким же, как если бы значение System. ItemType файла было передано в [**псформатфордисплай**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay).

Это свойство не следует путать с [System. Kind](./props-system-kind.md), которое представляет собой высокоуровневое понятное имя типа. Например, для DOC-файла документа используются различные свойства, как показано ниже.



| Свойство                                               | Значение                   |
|--------------------------------------------------------|-------------------------|
| [System. Kind](./props-system-kind.md)                 | Документ                |
| [System. ItemType](./props-system-itemtype.md)         | .doc                    |
| [System. Итемтипетекст]() | Документ Microsoft Word |



 

Примеры значений



| Путь                                   | итемтипетекст            |
|----------------------------------------|-------------------------|
| в. \\ \\ линейчатая диаграмма MyDir \\hello.txt              | Текстовый файл               |
| \\\\\\Общая папка сервера \\ MyDir \\goodnews.doc | Документ Microsoft Word |
| \\\\\\Общая \\ папка сервера              | Папка с файлами             |
| c: \\ MyDir \\ MyFolder                    | Папка с файлами             |
| Учетная запись/маилбокс/Inbox/"Re: Hello!"    | Сообщение электронной почты Outlook  |



 

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

 

 
