---
title: Простой тип Версионтипе
description: Определяет шаблон, указывающий версию задачи.
ms.assetid: e9eebbc1-5465-4af6-8b97-f1fd5827442e
keywords:
- планировщик задач простого типа Версионтипе
topic_type:
- apiref
api_name:
- versionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 52ad30f5ea14a447e2a08151ef2803b0577066e147e29673d373ce87eee033f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355040"
---
# <a name="versiontype-simple-type"></a>Простой тип Версионтипе

Определяет шаблон, указывающий версию задачи.

``` syntax
<xs:simpleType name="versionType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\d+(\.\d+){1,3}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Шаблоны

Простой тип **версионтипе** — это **строка** , которая ограничена следующим шаблоном:

-   `\d+(\.\d+){1,3}`

    Double, за которым следует один, два или три типа Double. Например, 1,2 или 1.2.3.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





