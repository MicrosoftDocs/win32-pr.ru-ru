---
description: 'Префикс элемента, используемый для сообщений электронной почты, в которых тема начинается с префикса &\# 0034; Re: &\# 0034;.'
ms.assetid: 3c257edc-b7f7-498d-8347-0be4fca41023
title: System. Итемнамепрефикс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd7830f63c3e9e0f6026099c95d11820a1d8592928cece72ebe72d76936d8467
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119598464"
---
# <a name="systemitemnameprefix"></a>System. Итемнамепрефикс

Префикс элемента, используемый для сообщений электронной почты, в которых тема начинается с префикса "Re:".

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemNamePrefix
   shellPKey = PKEY_ItemNamePrefix
   formatID = D7313FF1-A77A-401C-8C99-3DBDD68ADD36
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Remarks

Значения PKEY определены в списке PKEY. h.

Если элемент является файлом, значение этого свойства — VT \_ Empty. Если элемент является сообщением, то значением этого свойства являются префиксы перенаправления или отклика (включая двоеточие, но без пробелов) или VT \_ Empty, если префикс отсутствует.

Примеры значений



| System. Итемнамепрефикс | System. ItemName  | System.ItemNameDisplay |
|-----------------------|------------------|------------------------|
| VT \_ пуст             | "Отличный день"      | "Отличный день"            |
| "Re:"                 | "Отличный день"      | "Re: отличный день"        |
| "ФВД:"               | "Месячный бюджет" | "ФВД: месячный бюджет"  |
| VT \_ пуст             | accounts.xls     | accounts.xls           |



 

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

 

 
