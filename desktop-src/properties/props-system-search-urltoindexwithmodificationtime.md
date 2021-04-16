---
description: Это свойство аналогично System. Search. Урлтоиндекс, за исключением того, что оно включает время последнего изменения URL-адреса.
ms.assetid: 53ca765b-0795-49ab-9946-c3ef101ababd
title: System. Search. Урлтоиндексвисмодификатионтиме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fcc83b9796ae2375f10235a08ba0db313fb1958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712636"
---
# <a name="systemsearchurltoindexwithmodificationtime"></a>System. Search. Урлтоиндексвисмодификатионтиме

Это свойство аналогично [**System. Search. урлтоиндекс**](props-system-search-urltoindex.md) , за исключением того, что оно включает время последнего изменения URL-адреса. Это оптимизация индексатора, поэтому ему не нужно обращаться к обработчику протокола, чтобы запросить эти сведения, чтобы определить, нужно ли повторно индексировать содержимое.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.UrlToIndexWithModificationTime
   shellPKey = PKEY_Search_UrlToIndexWithModificationTime
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Any
```

## <a name="remarks"></a>Комментарии

Это свойство [System. Search. урлтоиндексвисмодификатионтиме]() совпадает со свойством [System. Search. урлтоиндекс](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) , за исключением того, что вы также передаете время последнего изменения документа. Если время последнего изменения совпадает, индексатор предполагает, что документ уже проиндексирован и не выдает уведомление. Это свойство является вектором с двумя элементами — значением **VT \_ LPWSTR** , которое содержит URL-адрес и значение **VT \_ fileTime** , которое содержит время последнего изменения.

[System. Search. урлтоиндексвисмодификатионтиме]() назывался PID \_ ГСР \_ дирлинк \_ с \_ временем в более ранних версиях операционной системы Windows.

Значения PKEY определены в списке PKEY. h.

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. Search. Урлтоиндекс](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))
</dt> <dt>

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

 

 
