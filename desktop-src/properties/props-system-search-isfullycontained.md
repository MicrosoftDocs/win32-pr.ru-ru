---
description: Порождено как ИСТИНное всеми дочерними элементами контейнера (например, электронной почтой или сжатым файлом с расширением ZIP), который создает System. Search. Исклоседдиректори как TRUE. Это гарантирует, что дочерние элементы будут включены в индекс поиска.
ms.assetid: 6da60e89-6956-41f6-8624-063c4d46464d
title: System. Search. Исфулликонтаинед
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1245f29a2940146a4e5d8f0a392210173be75e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546759"
---
# <a name="systemsearchisfullycontained"></a>System. Search. Исфулликонтаинед

Порождено как **истинное** всеми дочерними элементами контейнера (например, электронной почтой или сжатым файлом с расширением ZIP), который создает [System. Search. исклоседдиректори](./props-system-search-iscloseddirectory.md) как **true**. Это гарантирует, что дочерние элементы будут включены в индекс поиска.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.IsFullyContained
   shellPKey = PKEY_Search_IsFullyContained
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 24
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>Комментарии

Значения PKEY определены в списке PKEY. h.

Свойство [System. Search. исклоседдиректори](./props-system-search-iscloseddirectory.md) помогает оптимизировать производительность индексатора, позволяя индексатору пропустить перечисление дочерних элементов контейнера. Тем не менее эти дочерние элементы помечаются индексатором как не посещенный, поэтому они будут удалены из индекса. При выдаче [System. Search. исфулликонтаинед]() как **true** элемент не удаляется из индекса, несмотря на то, что он не был посещен.

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

 

 
