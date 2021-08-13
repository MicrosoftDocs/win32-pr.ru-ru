---
description: Прочитайте о свойстве System. Итемфолдерпасдисплайнарров, которое представляет понятный пользователю отображаемый путь к родительской папке элемента.
ms.assetid: f60b7465-bca4-4c7b-9caf-9cda1bf6eeeb
title: System. Итемфолдерпасдисплайнарров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb87cadc4f4f132870ea51af1bba55c992c09d3eb5a90f446a3d92810b5941d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118726491"
---
# <a name="systemitemfolderpathdisplaynarrow"></a>System. Итемфолдерпасдисплайнарров

Понятный пользователю отображаемый путь к родительской папке элемента.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemFolderPathDisplayNarrow
   shellPKey = PKEY_ItemFolderPathDisplayNarrow
   formatID = DABD30ED-0043-4789-A7F8-D013A4736622
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Remarks

Значения PKEY определены в списке PKEY. h.

Формат строки должен быть адаптирован таким образом, чтобы имя папки поступило в первую очередь, чтобы оптимизировать для такого столбца. Если папка является папкой файлов, то значение включает все локализованные имена. Если [System. итемфолдерпасдисплай](./props-system-itemfolderpathdisplay.md) является VT \_ пустым, это свойство также должно быть пустым. В противном случае он должен быть получен соответствующим образом источником данных из System. Итемфолдерпасдисплай.

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

 

 
