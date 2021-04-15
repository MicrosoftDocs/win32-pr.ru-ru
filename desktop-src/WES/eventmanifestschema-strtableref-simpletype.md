---
title: Простой тип Стртаблереф
description: Определяет строку, которая ссылается на строку сообщения, определенную в таблице строк в манифесте или в файле сообщения (. MC).
ms.assetid: ecbcefcb-3265-4508-be7d-17a0fe3fe911
keywords:
- Журнал событий простого типа Стртаблереф
topic_type:
- apiref
api_name:
- strTableRef
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95b7db446af056987e2aa25cd1483e9e53c01d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534385"
---
# <a name="strtableref-simple-type"></a>Простой тип Стртаблереф

Определяет строку, которая ссылается на строку сообщения, определенную в таблице строк в манифесте или в файле сообщения (. MC).

``` syntax
<xs:simpleType name="strTableRef">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Шаблоны

Простой тип **стртаблереф** — это **Строка типа xs: String** , которая ограничена следующим шаблоном:

-   `(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))`

    Строка должна иметь форму $string. *stringid* или $MC.*симболид*. Если строка имеет форму, $string. *stringid*, он должен ссылаться на строку в разделе [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) манифеста. Если строка имеет форму, $mc.*симболид*, она должна ссылаться на символ, определенный в файле сообщения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



 

 





