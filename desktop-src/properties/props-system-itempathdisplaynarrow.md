---
description: Понятный пользователю отображаемый путь к элементу.
ms.assetid: 5dd44e13-bc5c-4e32-b5eb-2c7c40e10dfb
title: System. Итемпасдисплайнарров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ef7b9d03a78a23e955c20f52e32062a8bcabd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265999"
---
# <a name="systemitempathdisplaynarrow"></a>System. Итемпасдисплайнарров

Понятный пользователю отображаемый путь к элементу.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemPathDisplayNarrow
   shellPKey = PKEY_ItemPathDisplayNarrow
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Комментарии

Значения PKEY определены в списке PKEY. h.

Чтобы оптимизировать для столбца с узким просмотром, формат строки должен быть адаптирован, чтобы имя было первым.

Если элемент является файлом, значение свойства исключает расширение файла, но включает локализованные имена, если они присутствуют. Если элемент является сообщением, то значение включает параметр [System. итемнамепрефикс](./props-system-itemnameprefix.md). Для синтаксического анализа пути к элементу используйте [System. итемурл](./props-system-itemurl.md) или [System. парсингпас](./props-system-parsingpath.md).

Примеры значений



| Путь                                   | итемпасдисплайнаме                 |
|----------------------------------------|-------------------------------------|
| в. \\ \\ линейчатая диаграмма MyDir \\hello.txt              | Привет (c: \\ MyDir \\ Bar)              |
| \\\\\\Общая папка сервера \\ MyDir \\goodnews.doc | гудневс ( \\ \\ Серверный \\ общий ресурс \\ MyDir) |
| \\\\\\Общая \\ папка сервера              | папка ( \\ \\ Общая папка сервера \\ )          |
| c: \\ MyDir \\ MyFolder                    | MyFolder (c: \\ MyDir)                |
| Учетная запись/маилбокс/Inbox/"Re: Hello!"    | Повтор: Привет! (Учетная запись/маилбокс/входящие) |



 

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

 

 
