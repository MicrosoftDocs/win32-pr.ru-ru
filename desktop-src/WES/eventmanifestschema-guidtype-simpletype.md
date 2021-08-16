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
ms.openlocfilehash: 0ff7d5b0b65e7c434b6281098531e4eae5e76cf1565b21f6b1a3ffbca46af37b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343728"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





