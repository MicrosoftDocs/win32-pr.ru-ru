---
description: Отображаемое имя в &\# 0034; наиболее полное&\# 0034; Form.
ms.assetid: fdb6b0fa-0741-4edc-8902-763a461313b9
title: System.ItemNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34e21c0ded147789cadccc99aaf9b2a1910398430419edacc498214c6489d77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119598474"
---
# <a name="systemitemnamedisplay"></a>System.ItemNameDisplay

Отображаемое имя в "наиболее полной" форме. Это уникальное представление имени элемента, наиболее подходящее для конечных пользователей.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemNameDisplay
   shellPKey = PKEY_ItemNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 10
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Remarks

Значения PKEY определены в списке PKEY. h.

Это значение равно конкатентатион для [System. итемнамепрефикс](./props-system-itemnameprefix.md) и [System. ItemName](./props-system-itemname.md).

Если элемент является файлом, это свойство содержит отображаемое имя, как показано в проводнике. Существуют допустимые случаи, когда указано свойство [System. имя_файла](./props-system-filename.md) , но значение этого свойства совершенно другое. Хорошим примером являются сообщения электронной почты. Если элемент является сообщением электронной почты, имя элемента обычно является темой. В этом случае значение должно быть объединением [System. итемнамепрефикс](./props-system-itemnameprefix.md) и [System. ItemName](./props-system-itemname.md). Поскольку значение System. Итемнамепрефикс исключает все конечные пробелы, при создании [System. итемнамедисплай]()сцепление должно включать пробел. Обратите внимание, что это свойство не обязательно должно быть уникальным, но оно предназначено для продвижения наиболее вероятного кандидата, который может быть уникальным и имеет смысл для конечных пользователей.

Например, для документов можно использовать [System. Title](./props-system-title.md) в качестве [System. итемнамедисплай](), но на практике заголовок документов может оказаться неполезным или уникальным для работы в качестве единственного System. итемнамедисплай. Вместо этого лучше предоставлять [System. filename](./props-system-filename.md) как значение System. итемнамедисплай. в Windows Mail электронная почта хранится в файловой системе в виде eml-файлов. Значения System. FileName для этих файлов не являются понятными, так как они являются идентификаторами GUID. В этом примере повышается смысл повышения уровня [System. subject](./props-system-subject.md) как System. итемнамедисплай.

**Примечания по совместимости:**

-   реализации папок оболочки в Windows Vista: используйте PKEY \_ итемнамедисплай для столбца name, если нужно, чтобы Windows Explorer вызывал [**ишеллфолдер:: жетдисплайнамеоф**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(шгдн \_ нормаль) для получения значения имени. используйте другой PKEY, например pkey \_ ItemName, если нужно, чтобы Windows Explorer вызывал либо хранилище свойств папки, либо [**IShellFolder2:: жетдетаилсекс**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) , чтобы получить значение имени.
-   реализации папок оболочки в Windows XP: первый столбец должен быть столбцом name, а Windows Explorer вызывает [**ишеллфолдер:: жетдисплайнамеоф**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) , чтобы получить значение имени. Значение PKEY/СЦИД не имеет значения.



| Тип элемента     | Пример                   |
|---------------|---------------------------|
| File          | hello.txt                 |
| Message       | Re: где находится собрание? |
| Папка устройства | песня. WMA                  |
| Папка        | Документы                 |



 

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

 

 
