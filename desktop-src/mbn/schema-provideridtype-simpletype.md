---
description: Определяет тип для элемента ProviderID профиля мобильного широкополосного подключения.
ms.assetid: 84193749-c98d-4313-bf99-3da1c74d7cc4
title: Простой тип Провидеридтипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerIdType
api_type:
- Schema
ms.openlocfilehash: ec3c952395be048d18305172e64618fa26313f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144788"
---
# <a name="provideridtype-simple-type"></a>Простой тип Провидеридтипе

Простой тип **провидеридтипе** определяет тип для элемента [**ProviderID**](schema-providerid-providertype-element.md) профиля мобильного широкополосного подключения. Этот тип представляет собой набор цифр длиной не менее одной цифры и не более 6 цифр.

``` syntax
<xs:simpleType name="providerIdType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="\d{1,6}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Шаблоны

Простой тип **провидеридтипе** — это токен, который ограничен следующим шаблоном:

-   `\d{1,6}`

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



 

 




