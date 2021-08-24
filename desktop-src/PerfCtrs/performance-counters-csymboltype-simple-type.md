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
ms.openlocfilehash: e4ebba4d72b7bc79f2aaefccfa2d71e57abd82aa06efb09abc2e83cebdb513f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033534"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 




