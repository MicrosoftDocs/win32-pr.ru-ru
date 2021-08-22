---
description: Определяет тип глобального уникального идентификатора в формате реестра.
ms.assetid: 2be73c57-b6b6-46ab-93e1-d70f8655c30e
title: Простой тип Гуидтипе (счетчики производительности)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 305195784a3578242caefc1fb7eb9bcd8dbd5b557d89d8752bc8242f648abbdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119624924"
---
# <a name="guidtype-simple-type-performance-counters"></a>Простой тип Гуидтипе (счетчики производительности)

Определяет тип глобального уникального идентификатора в формате реестра.

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Шаблоны

Простой тип **гуидтипе** — это **Строка типа xs: String** , которая ограничена следующим шаблоном:

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    Значение должно быть глобально уникальным идентификатором в формате реестра. Например, {5b2fc63a-8AF4-44cb-960c-aefdced908d6}. Для создания идентификатора GUID используйте GUIDGen.exe или UUIDGen.exe.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 




