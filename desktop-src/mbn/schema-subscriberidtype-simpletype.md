---
description: Определяет тип для элемента Субскриберид профиля мобильного широкополосного подключения.
ms.assetid: b36df4d3-f558-4af8-8f63-e4991c34990f
title: Простой тип Субскриберидтипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- subscriberIdType
api_type:
- Schema
ms.openlocfilehash: c3c776bbd721bbb03b4f5549f87d48248a35206b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072723"
---
# <a name="subscriberidtype-simple-type"></a>Простой тип Субскриберидтипе

Простой тип **субскриберидтипе** определяет тип для элемента [**Субскриберид**](schema-subscriberid-mbnprofile-element.md) профиля мобильного широкополосного подключения. Этот тип представляет собой коллекцию из одного или нескольких символов.

``` syntax
<xs:simpleType name="subscriberIdType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



 

 




