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
ms.openlocfilehash: aac83be84ae313f572d82e6b4c9a2afb14beeb7e15c531eaae7efd67bcc90464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881368"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



 

 




