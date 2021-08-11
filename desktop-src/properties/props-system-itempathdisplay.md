---
description: Прочитайте о свойстве System. Итемпасдисплай, которое представляет понятный пользователю отображаемый путь к элементу.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System. Итемпасдисплай
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a58d48740c6f7a2f9db0e496a951105c176ca7eba3dd205c2971188af7fd55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118231667"
---
# <a name="systemitempathdisplay"></a>System. Итемпасдисплай

Понятный пользователю отображаемый путь к элементу.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemPathDisplay
   shellPKey = PKEY_ItemPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 7
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Remarks

Значения PKEY определены в списке PKEY. h.

Если элемент является файлом или папкой, это свойство включает расширение во всех случаях и локализуется, если локализованное имя доступно. Для других элементов это понятный для пользователя эквивалент, предполагая, что элемент существует в иерархическом хранилище.

В отличие от [System. итемурл](./props-system-itemurl.md), это значение свойства не включает схему URL-адресов. Для синтаксического анализа пути к элементу используйте System. Итемурл или [System. парсингпас](./props-system-parsingpath.md). Для ссылки на элементы пространства имен оболочки с помощью интерфейсов API оболочки используйте System. Парсингпас.

Примеры значений



| Путь                                   | итемпасдисплай                        |
|----------------------------------------|----------------------------------------|
| в. \\ \\ линейчатая диаграмма MyDir \\hello.txt              | в. \\ \\ линейчатая диаграмма MyDir \\hello.txt              |
| \\\\\\Общая папка сервера \\ MyDir \\goodnews.doc | \\\\\\Общая папка сервера \\ MyDir \\goodnews.doc |
| \\\\\\Общая папка сервера \\numbers.xls         | \\\\\\Общая папка сервера \\numbers.xls         |
| c: \\ MyDir \\ MyFolder                    | c: \\ MyDir \\ MyFolder                    |
| Учетная запись/маилбокс/Inbox/"Re: Hello!"    | Учетная запись/маилбокс/Inbox/"Re: Hello!"    |



 

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

 

 
