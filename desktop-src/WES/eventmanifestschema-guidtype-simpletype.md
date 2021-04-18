---
title: Простой тип Гуидтипе (схема Евентманифест)
description: Определяет тип глобального уникального идентификатора в формате реестра. | Простой тип Гуидтипе (схема Евентманифест)
ms.assetid: c35fa54b-5a2e-46de-a1c7-fc408b00ee68
keywords:
- Журнал событий простого типа Гуидтипе
topic_type:
- apiref
api_name:
- GUIDType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 474715cf4e9c11536ca227ecdb5609b13be7e222
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694078"
---
# <a name="guidtype-simple-type-eventmanifest-schema"></a>Простой тип Гуидтипе (схема Евентманифест)

Определяет тип глобального уникального идентификатора в формате реестра.

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Шаблоны

Простой тип **гуидтипе** — это строка, которая ограничена следующим шаблоном:

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    Значение должно быть глобально уникальным идентификатором в формате реестра. Например, {5b2fc63a-8AF4-44cb-960c-aefdced908d6}. Для создания идентификатора GUID используйте GUIDGen.exe или UUIDGen.exe.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





