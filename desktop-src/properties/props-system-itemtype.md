---
description: Канонический тип элемента.
ms.assetid: 530ba98a-09fd-438b-8872-9eee47f0cf54
title: System. ItemType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0159a12e1cc3c6d85e461461cad20334a641fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272340"
---
# <a name="systemitemtype"></a>System. ItemType

Канонический тип элемента.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemType
   shellPKey = PKEY_ItemType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 11
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Комментарии

Значения PKEY определены в списке PKEY. h.

Значение System. ItemType предназначено для программного синтаксического анализа и может быть одним из следующих:

-   Расширение файла, которое указывает на значение ProgID ( \_ корень классов hKey \_ \\ <ProgID> ), содержащее отображаемое имя для типа.
-   Значение ProgID (HKEY \_ Classes \_ ррут \\ <ProgID> ), содержащее отображаемое имя для типа.

Элемент Фриендлитипенаме ProgID должен быть локализованной версией имени приложения ( @winword.dll -42), а значение по умолчанию для ключа ProgID — нелокализованным именем (Word.Docумент. 12).

Если канонического типа нет, это значение является VT \_ пустым. Если элемент является файлом ([System. filename](./props-system-filename.md) не является VT \_ ), то значение совпадает с [System. fileExtension](./props-system-fileextension.md). Используйте [System. итемтипетекст](./props-system-itemtypetext.md) , если нужно отобразить тип для конечных пользователей в представлении.

> [!Note]  
> Если элемент является файлом, передача значения [System. ItemType]() в [**псформатфордисплай**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) приведет к тому же значению, что и [System. итемтипетекст](./props-system-itemtypetext.md).

 

Примеры значений



| Путь                                   | ItemType         |
|----------------------------------------|------------------|
| в. \\ \\ линейчатая диаграмма MyDir \\hello.txt              | .txt             |
| \\\\\\Общая папка сервера \\ MyDir \\goodnews.doc | .doc             |
| \\\\\\Общая \\ папка сервера              | Каталог        |
| c: \\ MyDir \\ MyFolder                    | Каталог        |
| \[desktop\]                            | Папка           |
| Учетная запись/маилбокс/Inbox/"Re: Hello!"    | MAPI/IPM. Сообщение |



 

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
</dt> <dt>

[Программные идентификаторы](../shell/fa-progids.md)
</dt> </dl>

 

 
