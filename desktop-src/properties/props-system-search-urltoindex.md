---
description: Создается контейнером IFilter для каждого дочернего URL-адреса в контейнере. В итоге дочерние элементы обрабатываются индексатором, если они находятся в пределах области.
ms.assetid: e864b3fa-6d43-40fe-9556-474953098947
title: System. Search. Урлтоиндекс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4832279237cb7a3659b37d6502bd853caff113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712136"
---
# <a name="systemsearchurltoindex"></a>System. Search. Урлтоиндекс

Создается контейнером [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) для каждого дочернего URL-адреса в контейнере. В итоге дочерние элементы обрабатываются индексатором, если они находятся в пределах области.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.UrlToIndex
   shellPKey = PKEY_Search_UrlToIndex
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
```

## <a name="remarks"></a>Комментарии

Это свойство содержит URL-адрес и порождается обработчиком протокола для каждого дочернего URL-адреса или директой под текущим URL-адресом. Индексатор обращается к обработчику протокола и запрашивает индексирование этого документа. [System. Search. урлтоиндекс](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) назывался PID \_ ГСР \_ дирлинк в более ранних версиях операционной системы Windows.

Значения PKEY определены в списке PKEY. h.

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. Search. Урлтоиндексвисмодификатионтиме](./props-system-search-urltoindexwithmodificationtime.md)
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

 

 
