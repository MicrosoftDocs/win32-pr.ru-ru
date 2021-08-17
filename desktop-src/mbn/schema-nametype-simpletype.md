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
ms.openlocfilehash: 9b07bfb62e23b0c82ef69bc924147675caad10d61258a5c49edc906c4b6bf2a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881408"
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
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



 

 




