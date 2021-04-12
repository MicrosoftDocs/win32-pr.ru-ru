---
description: Для этой строки должна быть задана фонетическая версия отображаемого имени, определенная в System. Итемнамедисплай в языковых стандартах CJK (CHS пиньинь, JPN хирагана, KOR хангыль и т. д.).
ms.assetid: eb491644-bf59-4439-9e9b-bcafde619d66
title: System. Итемнамесортоверриде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79f9bb07eb15eb5d25fbfa1e95d4c0f80b35611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265691"
---
# <a name="systemitemnamesortoverride"></a>System. Итемнамесортоверриде

Для этой строки должна быть задана фонетическая версия отображаемого имени, определенная в System. Итемнамедисплай в языковых стандартах CJK (CHS пиньинь, JPN хирагана, KOR хангыль и т. д.). Первый символ этого поля также используется для группирования имен по фирстлеттер. Для большинства языков, отличных от CJK, это поле задавать не нужно (в этом случае будет использоваться System. Итемнамедисплай). Однако если желательно переопределить букву группировки (например, чтобы удалить ведущие статьи, например "a" и "The"), здесь можно указать альтернативную строку.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8

```
propertyDescription
   name = System.ItemNameSortOverride
   shellPKey = PKEY_ItemNameSortOverride
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Комментарии

Значения PKEY определены в списке PKEY. h.

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

 

 
