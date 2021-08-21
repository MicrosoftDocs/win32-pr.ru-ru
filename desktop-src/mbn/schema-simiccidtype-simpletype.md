---
description: Определяет тип для элемента СимикЦид профиля мобильного широкополосного подключения.
ms.assetid: ce77180e-71e2-4cef-84e0-32397216385f
title: Простой тип СимикЦидтипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- simIccIDType
api_type:
- Schema
ms.openlocfilehash: 33a984875e1e6840787d81dc53c8fc13ead54a0328f6610d75c30075066c13c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035762"
---
# <a name="simiccidtype-simple-type"></a>Простой тип СимикЦидтипе

Простой тип **симикЦидтипе** определяет тип для элемента [**СимикЦид**](schema-simiccid-mbnprofile-element.md) профиля мобильного широкополосного подключения. Этот тип представляет собой набор цифр и (или) букв верхнего и нижнего регистра, по крайней мере один символ и длину не более 20 символов.

``` syntax
<xs:simpleType name="simIccIDType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="[a-zA-Z\d]{1,20}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Шаблоны

Простой тип **симикЦидтипе** — это токен, который ограничен следующим шаблоном:

-   `[a-zA-Z\d]{1,20}`

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



 

 




