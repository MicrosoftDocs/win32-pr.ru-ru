---
description: Определяет тип строки для профиля мобильного широкополосного подключения.
ms.assetid: a5c14c39-2731-44f0-9fd2-e78d900b66f0
title: простой тип Наметипе (мобильное широкополосное подключение)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
ms.openlocfilehash: d8c6032e17eaf2d067dc23030a7a6279bd41eafa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662415"
---
# <a name="nametype-simple-type-mobile-broadband"></a>простой тип Наметипе (мобильное широкополосное подключение)

Простой тип **наметипе** определяет строковый тип для профиля мобильного широкополосного подключения. Эта строка состоит по меньшей мере из одного символа и не длиннее 255 символов.

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



 

 




