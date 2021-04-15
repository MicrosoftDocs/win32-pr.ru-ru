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
ms.openlocfilehash: 410145e659a4845c9c96aaeb76d522de3e0c7b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662409"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



 

 




