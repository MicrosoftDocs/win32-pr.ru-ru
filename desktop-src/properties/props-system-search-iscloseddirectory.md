---
description: Порождено как ИСТИНное элементом контейнера, чтобы показать, что его дочерние элементы не должны перечисляться индексатором, если элемент контейнера не был изменен с момента последнего сканирования при добавочном сканировании индекса.
ms.assetid: 8bb487b9-4a51-4a6b-939e-946a8aad85de
title: System. Search. Исклоседдиректори
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea97aeb8d0192eea7d71ca65fd0ec109780702f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719662"
---
# <a name="systemsearchiscloseddirectory"></a>System. Search. Исклоседдиректори

Порождено как **истинное** элементом контейнера, чтобы показать, что его дочерние элементы не должны перечисляться индексатором, если элемент контейнера не был изменен с момента последнего сканирования при добавочном сканировании индекса. Это способствует оптимизации производительности индексатора. В этих вариантах контейнеров (примерах являются сообщения электронной почты с вложениями или сжатый файл с расширением ZIP), дочерние элементы могли от родительского элемента. Например, если свойство [System. DateModified](./props-system-datemodified.md) содержащегося элемента изменяется, значение System. DateModified контейнера изменяется на Match. Кроме того, при удалении родительского элемента также удаляются и все дочерние элементы. Таким образом, если контейнер не изменился, индексатор знает, что в нем ничего не изменилось и ему не нужно открывать контейнер для проверки содержимого по отдельности.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.IsClosedDirectory
   shellPKey = PKEY_Search_IsClosedDirectory
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>Комментарии

Значения PKEY определены в списке PKEY. h.

> [!IMPORTANT]
> Если элемент порождает **значение true** для этого свойства, все его дочерние элементы должны порождать свойство [System. Search. исфулликонтаинед](./props-system-search-isfullycontained.md) как **true** , чтобы предотвратить удаление этих элементов из индекса.

 

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

 

 
