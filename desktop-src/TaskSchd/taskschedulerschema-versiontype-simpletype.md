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
ms.openlocfilehash: df7010c6ecba29ad0ade80ce403018dd626d01cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340485"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





