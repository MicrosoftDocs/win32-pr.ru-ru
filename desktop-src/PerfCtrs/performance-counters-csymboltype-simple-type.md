---
description: Простой тип Ксимболтипе (счетчики производительности) — определяет допустимое имя символа C/C++.
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Простой тип Ксимболтипе (счетчики производительности)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0771bb1dffc006abf8e02e6c391278f7d0b03f11
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084232"
---
# <a name="csymboltype-simple-type-performance-counters"></a>Простой тип Ксимболтипе (счетчики производительности)

Определяет допустимое имя символа C/C++.

``` syntax
<xs:simpleType name="CSymbolType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="()|([_a-zA-Z][_0-9a-zA-Z]*)"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Шаблоны

Простой тип **ксимболтипе** — это **Строка типа xs: String** , которая ограничена следующим шаблоном:

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    Имя символа может быть пустым или содержать буквы, цифры и символы подчеркивания. Если указано имя, имя должно начинаться с символа подчеркивания ( \_ ) или алфавитного знака.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 




