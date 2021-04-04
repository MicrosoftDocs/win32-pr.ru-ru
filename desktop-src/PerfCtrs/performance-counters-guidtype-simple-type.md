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
ms.openlocfilehash: 758509a564c26db493fa2e9ed971aba71878cdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909716"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 




